<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [obsidian](./obsidian.md) &gt; [TextFileView](./obsidian.textfileview.md)

## TextFileView class

This class implements a plaintext-based editable file view, which can be loaded and saved given an editor.

Note that by default, this view only saves when it's closing. To implement auto-save, your editor should call `this.requestSave()` when the content is changed.

**Signature:**

```typescript
export abstract class TextFileView extends EditableFileView 
```
**Extends:** [EditableFileView](./obsidian.editablefileview.md)

## Constructors

|  Constructor | Modifiers | Description |
|  --- | --- | --- |
|  [(constructor)(leaf)](./obsidian.textfileview._constructor_.md) |  | Constructs a new instance of the <code>TextFileView</code> class |

## Properties

|  Property | Modifiers | Type | Description |
|  --- | --- | --- | --- |
|  [data](./obsidian.textfileview.data.md) |  | string | In memory data |
|  [requestSave](./obsidian.textfileview.requestsave.md) |  | () =&gt; void | Debounced save in 2 seconds from now |

## Methods

|  Method | Modifiers | Description |
|  --- | --- | --- |
|  [clear()](./obsidian.textfileview.clear.md) | <code>abstract</code> | Clear the editor. This is usually called when we're about to open a completely different file, so it's best to clear any editor states like undo-redo history, and any caches/indexes associated with the previous file contents. |
|  [getViewData()](./obsidian.textfileview.getviewdata.md) | <code>abstract</code> | Gets the data from the editor. This will be called to save the editor contents to the file. |
|  [onLoadFile(file)](./obsidian.textfileview.onloadfile.md) |  |  |
|  [onUnloadFile(file)](./obsidian.textfileview.onunloadfile.md) |  |  |
|  [save(clear)](./obsidian.textfileview.save.md) |  |  |
|  [setViewData(data, clear)](./obsidian.textfileview.setviewdata.md) | <code>abstract</code> | <p>Set the data to the editor. This is used to load the file contents.</p><p>If clear is set, then it means we're opening a completely different file. In that case, you should call clear(), or implement a slightly more efficient clearing mechanism given the new data to be set.</p> |
