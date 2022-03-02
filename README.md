# @iconsauce/mdi-svg

This plugin scrapes [Material Icons](https://github.com/material-icons/material-icons) of [@material-icons/svg](https://github.com/material-icons/material-icons) from which contains official Google SVG versions.

For more infos go to [iconsauce docs][iconsauce-docs].

```js
module.exports = {
  content: [
    './src/**/*.{tsx,ts}',
  ],
  fontSize: '24px',
  plugin: [
    require('@iconsauce/material-icons'),
  ],
}
```

You will be able to use these icons in your project.

```jsx
const MyComponent = () => {

  const icon = 'mi/baseline/grass'

  return <section className={ icon }>
    <div className="grid desktop:grid-cols-4 mi/baseline/emoticon-happy tablet:grid-cols-2 grid-cols-1 desktop:gap-6 gap-12 desktop:auto-rows-fr desktop:items-end">
      <i className="mi/baseline/access-point"/>
      <span className='bg-adjust-tone-01/24 mi/baseline/terminal'/>
      <div>
        <footer title="mi/baseline/gondola"></footer>
      </div>
    </div>
  </section>
}
export default MyComponent
```

This plug-in will generate only icons used:

```css
@font-face {
  font-family: "iconsauce";
  src: url("data:font/truetype;charset=utf-8;base64,A...Z") format("truetype");
}

[class^="mi/"], [class*=" mi/"] {
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  font-family: "iconsauce" !important;
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 1;
}

.mi\/access-point::before { content: "\ea01" }
.mi\/emoticon-happy::before { content: "\ea02" }
.mi\/gondola::before { content: "\ea03" }
.mi\/grass::before { content: "\ea04" }
.mi\/harddisk::before { content: "\ea05" }
```

[iconsauce-docs]: https://iconsauce.github.io/docs/
