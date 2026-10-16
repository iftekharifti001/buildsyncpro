# BuildSync Pro — Gaming PC Builder

Functional, logic-driven PC builder (React + TypeScript + Tailwind).

## Engines (`src/logic/engine.ts`)
- **Compatibility**: CPU socket vs board socket, RAM type vs board type, CPU mem-controller vs board/RAM. Returns explicit issues.
- **Performance score**: `(cpuTier*0.4 + gpuTier*0.6) * 10` → 10–100.
- **Bottleneck**: `|cpuTier - gpuTier| * 10%`. diff ≥ 2 → bottleneck warning (CPU or GPU side).
- **PSU**: `(cpuTDP + gpuTDP + 100) * 1.2` → round up to `[450,550,650,750,850,1000,1200]`.

## Run
```
npm install
npm run dev
```
