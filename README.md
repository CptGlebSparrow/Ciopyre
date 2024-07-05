const createLoop = (onStep, timeout) => {
  let running = false

  const iteration = () => {
    onStep()
    if (running) setTimeout(iteration, timeout)
  }

  const start = () => {
    running = true
    iteration()
  }

  const stop = () => {
    running = false
  }

  return { start, stop }
}

const mainLoop = createLoop(() => {
  console.log('test')
}, 100)
def difference_by(a, b, fn):
    b = set(map(fn, b))
    return [item for item in a if fn(item) not in b]
let data = [
  [1, 2, 3, 4, 5],
  ['a', 'b', 'c', 'd', 'i'],
]
console.log(
  data.map((row) => {
    return `<tr>${row
      .map((col) => {
        return `<td>${col}</td>`
      })
      .join('')}</tr>`
  }),
)
