# AWS CLI 정리

### 업로드/다운로드

1. EC2에서 S3로 업로드하기

```jsx
aws s3 cp /local/object s3://bucket/to/object/path
```

![Screenshot 2022-09-04 at 12.23.37 PM.png](AWS%20CLI%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%85%E1%85%B5%20654f276a11204fa28e37d6f88b558484/Screenshot_2022-09-04_at_12.23.37_PM.png)

1. S3에서 EC2로 다운로드하기

```jsx
aws s3 cp s3://bucket/from/object/path /local/to/path
```

![Screenshot 2022-09-04 at 12.26.23 PM.png](AWS%20CLI%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%85%E1%85%B5%20654f276a11204fa28e37d6f88b558484/Screenshot_2022-09-04_at_12.26.23_PM.png)

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