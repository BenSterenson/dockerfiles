
FROM demisto/btfl-soup:1.0.1.4711

COPY requirements.txt .

RUN apk add --update --no-cache libxslt libxml2

RUN apk --update add --no-cache --virtual .build-dependencies python-dev build-base wget git \
  g++ gcc libxslt-dev \
  && pip install --no-cache-dir -r requirements.txt \
  && apk del .build-dependencies
