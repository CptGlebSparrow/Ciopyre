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
from math import floor


difference_by([2.1, 1.2], [2.3, 3.4],floor) # [1.2]
difference_by([{ 'x': 2 }, { 'x': 1 }], [{ 'x': 1 }], lambda v : v['x']) # [ { x: 2 } ]

difference([1, 2, 3], [1, 2, 4]) # [3]
