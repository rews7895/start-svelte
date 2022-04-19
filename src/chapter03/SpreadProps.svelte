<script>
  export let name;
  export let version;
  export let speed;
  export let website;
</script>

<div>
  <h1>03-3. Spread Props</h1>
  <p>객체를 넘길 경우 각 속성을 지정해서 전달하는 대신 ...pkg와 같이 전달할 수 있다.</p>
  <p>
    The <code>{name}</code> package is {speed} fast.
    Download version {version} from 
    <a href="https://www.npmjs.com/package/{name}">npm</a>
    and <a href={website}>learn more here</a>
  </p>
</div>