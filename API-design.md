**Tweet schema**
```
{
  id: string,
  text: string,
  userId: string,
  createdAt: Date,
}
```
**User schema**
```
{
  id: string,
  name: string,
  url: string,
  createdAt: Date,
}
```

**GET /tweets**

     전체 트윗 리스트를 가져온다.
     
     parameter: userName

     Response:

          - 200 : OK [tweet, tweet...]

          - 400 : Bad Request
          
          - 401: Unauthorized

          - 403 : Forbidden

          - 404 : Not Found


**POST /tweets**

    새로운 트윗을 생성한다.
    
    Request Body:
        {
          id: string,
          userId: string,
          text: string
        }
    
     Response:

      - 200 : OK

      - 400 : Bad Request
     
      - 401 : Unauthorized

      - 403 : Forbidden

      - 404 : Not Found
      
      - 409 : Conflict

**PUT /tweets/:id**

    트윗 내용을 수정한다.
    
    Request Body:
      {
        id: string (read only),
        userId: string (read only),
        text: string
      }
    
     Response:

      - 200 : OK

      - 400 : Bad Request
      
      - 401 : Unauthorized

      - 403 : Forbidden

      - 404 : Not Found

**DELETE /tweets/:id**

    트윗을 삭제한다.
    
     Response:

      - 200 : OK

      - 400 : Bad Request
      
      - 401 : Unauthorized

      - 403 : Forbidden

      - 404 : Not Found
