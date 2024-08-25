# Force HTTPS

`force-https` 中间件可以强制所有的请求转向至使用 HTTPS 协议.

此中间价如果应用于 `Router` 则只有在路由匹配到时才会强制转换协议，如果遇到页面不存在的情况，则不会转向.

但更常见的需求是期望任何的请求都自动转向，即使在路由未能匹配，返回 `404` 错误时，这时候可以把中间件添加到 `Service` 上. 不管请求是否被路由成功匹配， `Service` 上添加的中间件总是会执行.

_**示例代码**_ 

<CodeGroup>
  <CodeGroupItem title="main.rs" active>

@[code rust](../../../../codes/force-https/src/main.rs)

  </CodeGroupItem>
  <CodeGroupItem title="Cargo.toml">

@[code rust](../../../../codes/force-https/Cargo.toml)

  </CodeGroupItem>
</CodeGroup>