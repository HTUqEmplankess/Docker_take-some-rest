FROM node:18-alpine AS base

COPY . /app

# Build Next.js based on the preferred package manager
RUN cd /app; npm install --production
 
# Environment variables must be redefined at run time
ARG ENV_VARIABLE
ENV ENV_VARIABLE=${ENV_VARIABLE}
ARG NEXT_PUBLIC_ENV_VARIABLE
ENV NEXT_PUBLIC_ENV_VARIABLE=${NEXT_PUBLIC_ENV_VARIABLE}

EXPOSE 3000

CMD ["npm", "strat"]