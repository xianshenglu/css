want to preview demo?

please execute the code below at the console.

```
window.open(getPreviewUrl())

function getPreviewUrl(filename = 'index.html') {
  let urlArr = [...window.location.href.split('/'), filename]
  urlArr.splice(urlArr.findIndex(v => v === 'tree'), 2)
  let githubIndex = urlArr.findIndex(v => v === 'github.com')
  urlArr.splice(githubIndex, 2, urlArr[githubIndex + 1] + '.github.io')
  return urlArr.join('/')
}
```
