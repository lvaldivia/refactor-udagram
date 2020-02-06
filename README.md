# Container + Kubernetes

To use this images you have to configure enviromental variables like this:

export $POSTGRESS_HOST=url of your host\
export $POSTGRESS_USERNAME=username of your db\
export $POSTGRESS_PASSWORD=password of your db\
export $POSTGRESS_DB=name of your db\
export $AWS_REGION=region of your S3\
export $AWS_BUCKET=name of the bucke in S3\
export $AWS_PROFILE=name of the profile of aws configured in AWS Cli\
export $HOME=path of your aws credentials

#Udacity Rest Api Feed

docker run --rm --publish 8080:8080 -v $HOME/.aws:/root/.aws --env POSTGRESS_HOST=$POSTGRESS_HOST --env POSTGRESS_USERNAME=$POSTGRESS_USERNAME --env POSTGRESS_PASSWORD=$POSTGRESS_PASSWORD --env POSTGRESS_DB=$POSTGRESS_DB --env AWS_REGION=$AWS_REGION --env AWS_PROFILE=$AWS_PROFILE --env AWS_BUCKET=$AWS_BUCKET --env JWT_SECRET=$JWT_SECRET --name feed lvaldiva/udacity-restapi-feed

#Udacity Rest Api User

docker run --rm --publish 8080:8080 -v $HOME/.aws:/root/.aws --env POSTGRESS_HOST=$POSTGRESS_HOST --env POSTGRESS_USERNAME=$POSTGRESS_USERNAME --env POSTGRESS_PASSWORD=$POSTGRESS_PASSWORD --env POSTGRESS_DB=$POSTGRESS_DB --env AWS_REGION=$AWS_REGION --env AWS_PROFILE=$AWS_PROFILE --env AWS_BUCKET=$AWS_BUCKET --env JWT_SECRET=$JWT_SECRET --name user lvaldiva/udacity-restapi-user


