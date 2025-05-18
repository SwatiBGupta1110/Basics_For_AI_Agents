from pydantic import BaseModel

class User(BaseModel):
    id: int
    name: str
    signup_ts: str | None = None
    friends: list[int] = []

user = User(id='123', name='John', friends=[1, '2', b'3'])
print(user)
