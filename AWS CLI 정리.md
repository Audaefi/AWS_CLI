# AWS CLI 정리

### 업로드/다운로드

1. EC2에서 S3로 업로드하기

```jsx
aws s3 cp /local/object s3://bucket/to/object/path
```

![1.png](AWS CLI 정리/1.png)

1. S3에서 EC2로 다운로드하기

```jsx
aws s3 cp s3://bucket/from/object/path /local/to/path
```

![2.png](AWS CLI 정리/2.png)

### Bucket 생성/삭제

1. Bucket 생성하기

```jsx
aws s3 mb s3://bucket
```

1. Bucket 삭제하기

```jsx
aws s3 rb s3://bucket
```

### Bucket 내, 오브젝트 삭제

```jsx
aws s3 rm s3://bucket/to/path
```

### Bucket 내, 목록보기

```jsx
aws s3 ls s3://bucket/to/path
```

### 동기화 (Sync)

local to s3, s3 to local, s3 to s3를 지원함.

```jsx
aws s3 sync /local/from/path s3://bucket/to/path
aws s3 sync s3://bucket/from/path /local/to/path
aws s3 sync s3://bucket/from/path s3://bucket/to/path
```
