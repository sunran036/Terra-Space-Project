# Terra-Space-Project

20240603  
플레이어 이동 완성  
플레이어한테 카메라가 따라다님

```
using System.Collections; //상하좌우로 이동할수 있게 해주는 코드입니다. 요기부터
using System.Collections.Generic;
using TreeEditor;
using UnityEngine;

public class Player : MonoBehaviour
{   
    float x;
    float y;
    public float moveSpeed;
    Vector3 moveDirection;
    // Start is called before the first frame update
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        x = Input.GetAxisRaw("Horizontal");
        y = Input.GetAxisRaw("Vertical");

        moveDirection = new Vector3(x, y, 0);
        transform.position += moveDirection * moveSpeed * Time.deltaTime;
    }
} //여기까지
```


