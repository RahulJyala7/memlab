---
id: "heap_analysis_src.ObjectShallowAnalysis"
title: "Class: ObjectShallowAnalysis"
sidebar_label: "ObjectShallowAnalysis"
custom_edit_url: null
---

## Hierarchy

- [`BaseAnalysis`](heap_analysis_src.BaseAnalysis.md)

  ↳ **`ObjectShallowAnalysis`**

## Constructors

### <a id="new objectshallowanalysis"></a>**new ObjectShallowAnalysis**()

## Methods

### <a id="analyzesnapshotfromfile"></a>**analyzeSnapshotFromFile**(`file`)

Run heap analysis for a single heap snapshot file

 * **Parameters**:
    * `file`: `string` | the absolute path of a `.heapsnapshot` file.
 * **Returns**: `Promise`<`void`\> | this API returns void. To get the analysis results,
check out the documentation of the hosting heap analysis class and
call the analysis-specific API to get results after calling this method.
* **Example**:
```typescript
const analysis = new StringAnalysis();
await anaysis.analyzeSnapshotFromFile(snapshotFile);
const stringPatterns = analysis.getTopDuplicatedStringsInCount();
```

 * **Source**:
    * heap-analysis/src/BaseAnalysis.ts:75

___

### <a id="getcommandname"></a>**getCommandName**()

get CLI command name for this memory analysis;
use it with `memlab analyze <ANALYSIS_NAME>` in CLI

 * **Returns**: `string` | command name

 * **Source**:
    * heap-analysis/src/plugins/ObjectShallowAnalysis.ts:65

___

### <a id="gettopduplicatedobjectincount"></a>**getTopDuplicatedObjectInCount**()

get the top duplicated object in terms of duplicated object count

 * **Returns**: `ObjectRecord`[] | an array of the top-duplicated objects' information

 * **Source**:
    * heap-analysis/src/plugins/ObjectShallowAnalysis.ts:106
