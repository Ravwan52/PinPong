# PinPong C#
using UnityEngine;

public class Paddle : MonoBehaviour
{
    public float speed = 10f; // Скорость перемещения
    public string inputAxis; // Название оси ввода

    private Rigidbody2D rb;

    void Start()
    {
        rb = GetComponent<Rigidbody2D>();
    }

    void Update()
    {
        float move = Input.GetAxis(inputAxis); // Получаем ввод игрока
        rb.velocity = new Vector2(0, move * speed); // Двигаем ракетку
    }
}
