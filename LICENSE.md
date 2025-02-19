```csharp

using UnityEngine;

public class MovP2player : MonoBehaviour
{
    public float velocidade = 2.5f;
    public int pontuacao;
    
    void Start()
    {
        Debug.Log("Hello world");
    }

    void Update()
    {
        if (Input.GetKey(KeyCode.RightArrow) || Input.GetKey(KeyCode.D))
        {
            Debug.Log("tecla da seta para direita foi clicada");
            transform.Translate(new Vector3(velocidade * Time.deltaTime, 0, 0));
        }

        if (Input.GetKey(KeyCode.LeftArrow) || Input.GetKey(KeyCode.A))
        {
            Debug.Log("tecla da seta para esquerda foi clicada");
            transform.Translate(new Vector3(-velocidade * Time.deltaTime, 0, 0));
        }

        if (Input.GetKey(KeyCode.UpArrow) || Input.GetKey(KeyCode.W))
        {
            Debug.Log("tecla da seta para cima foi clicada");
            transform.Translate(new Vector3(0, 0, velocidade * Time.deltaTime));
        }

        if (Input.GetKey(KeyCode.DownArrow) || Input.GetKey(KeyCode.S))
        {
            Debug.Log("tecla da seta para baixo foi clicada");
            transform.Translate(new Vector3(0, 0, -velocidade * Time.deltaTime));
        }

        if (Input.GetKey(KeyCode.Z))
        {
            Debug.Log("tecla z foi clicada");
            pontuacao += 10;
            Debug.Log("a sua pontuação é de = " + pontuacao);
        }

        if (Input.GetKey(KeyCode.X))
        {
            Debug.Log("tecla x foi clicada");
            pontuacao -= 10;
            Debug.Log("a sua pontuação é de = " + pontuacao);
        }

        if (pontuacao == 100)
        {
            Debug.Log("Você chegou na pontuação máxima");
        }
    }
}
```
