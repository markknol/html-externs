# js.html Extern Generator

This project generates Haxe externs based on WebIDL files. The WebIDL
files and parser are owned by Mozilla.

# Usage

You should have the Haxe repository in a directory named "haxe" next to
this repo.

Run `bin/generate` to update the js.html externs on the Haxe repo. Run
`bin/validate` to make sure the output compiles.

To update to Mozilla's latest APIs, run `bin/update-mozilla` and run
generate again. You may also need to grab the latest WebIDL.py from
https://dxr.mozilla.org/mozilla-central/source/dom/bindings/parser/WebIDL.py

To add a new API by hand, add it in a new .webidl file under the webidl/
directory.

Any hand-written Haxe files that should be merged with the final output
should go in the haxe/ directory.

# Haxe 3.2 API migration

The following types from js.html have been removed, along with an
explanation. Most of the changes are due to spec advances, and removal
of Chrome-only APIs.

- js.html.Element
	- Renamed to HTMLElement
- js.html.HtmlElement
	- Renamed to HTMLHtmlElement

- js.html.AbstractWorker
    - Merged into Worker.
- js.html.AnimationList
    - ?
- js.html.BarInfo
    - Renamed to BarProp.
- js.html.BaseFontElement
    - Obsolete.
- js.html.BeforeLoadEvent
    - ?
- js.html.CSSFilterValue
    - ?
- js.html.CSSKeyframeRule
    - ?
- js.html.CSSKeyframesRule
    - ?
- js.html.CSSMatrix
    - Renamed to DOMMatrix.
- js.html.CSSTransformValue
    - ?
- js.html.CanvasRenderingContext
    - Obsolete.
- js.html.ClientRect
    - Renamed to DOMRect.
- js.html.ClientRectList
    - Renamed to DOMRectList.
- js.html.Clipboard
    - Renamed to DataTransfer.
- js.html.Counter
    - ?
- js.html.DOMApplicationCache
    - Renamed to ApplicationCache.
- js.html.DOMCoreException
    - Renamed to DOMException.
- js.html.DOMFormData
    - Renamed to FormData.
- js.html.DOMMimeType
    - Renamed to MimeType.
- js.html.DOMMimeTypeArray
    - Renamed to MimeTypeArray.
- js.html.DOMPlugin
    - Renamed to Plugin.
- js.html.DOMPluginArray
    - Renamed to PluginArray.
- js.html.DOMSelection
    - Renamed to Selection.
- js.html.DOMURL
    - Renamed to URL.
- js.html.DOMWindow
    - Renamed to Window.
- js.html.DataTransferItem
    - Obsolete.
- js.html.DataTransferItemList
    - Obsolete.
- js.html.DedicatedWorkerContext
    - Obsolete.
- js.html.DetailsElement
    - ?
- js.html.ElementTimeControl
    - ?
- js.html.Entity
    - Obsolete.
- js.html.EntityReference
    - Obsolete.
- js.html.EventException
    - ?
- js.html.GamepadList
    - Obsolete.
- js.html.Geoposition
    - Renamed to Position.
- js.html.JavaScriptCallFrame
    - ?
- js.html.KeygenElement
    - ?
- js.html.MarqueeElement
    - Obsolete.
- js.html.MediaController
    - ?
- js.html.MediaKeyEvent
    - ?
- js.html.MediaQueryListListener
    - ?
- js.html.MemoryInfo
    - Obsolete.
- js.html.MessageChannel
    - ?
- js.html.NamedFlow
    - ?
- js.html.Notation
    - Obsolete.
- js.html.NotificationCenter
    - Obsolete.
- js.html.OverflowEvent
    - ?
- js.html.PagePopupController
    - Obsolete.
- js.html.Point
    - Renamed to DOMPoint.
- js.html.RangeException
    - ?
- js.html.ScriptProfile
    - Obsolete.
- js.html.ScriptProfileNode
    - Obsolete.
- js.html.SharedWorkerContext
    - Obsolete.
- js.html.SpeechInputEvent
    - Renamed to SpeechRecognitionEvent.
- js.html.SpeechInputResult
    - Renamed to SpeechRecognitionResult.
- js.html.SpeechInputResultList
    - Renamed to SpeechRecognitionResultList.
- js.html.StorageInfo
    - Obsolete.
- js.html.StyleMedia
    - ?
- js.html.TextEvent
    - ?
- js.html.TextTrackCue
    - Renamed to VTTCue.
- js.html.WorkerContext
    - Obsolete.
- js.html.XMLHttpRequestException
    - ?
- js.html.XMLHttpRequestProgressEvent
    - ?
- js.html.XPathException
    - ?
- js.html.audio.AudioGain
    - Obsolete.
- js.html.audio.AudioSourceNode
    - Obsolete.
- js.html.audio.WaveTable
    - Obsolete.
- js.html.fs.DirectoryEntry
    - Obsolete.
- js.html.fs.DirectoryEntrySync
    - Obsolete.
- js.html.fs.DirectoryReader
    - Obsolete.
- js.html.fs.DirectoryReaderSync
    - Obsolete.
- js.html.fs.Entry
    - Obsolete.
- js.html.fs.EntryArray
    - Obsolete.
- js.html.fs.EntryArraySync
    - Obsolete.
- js.html.fs.EntrySync
    - Obsolete.
- js.html.fs.FileEntry
    - Obsolete.
- js.html.fs.FileEntrySync
    - Obsolete.
- js.html.fs.FileError
    - Obsolete.
- js.html.fs.FileException
    - Obsolete.
- js.html.fs.FileSystem
    - Obsolete.
- js.html.fs.FileSystemSync
    - Obsolete.
- js.html.fs.FileWriter
    - Obsolete.
- js.html.fs.FileWriterSync
    - Obsolete.
- js.html.fs.Metadata
    - Obsolete.
- js.html.idb.Any
    - Obsolete.
- js.html.idb.DatabaseException
    - Obsolete.
- js.html.idb.Key
    - Obsolete.
- js.html.idb.UpgradeNeededEvent
    - Obsolete.
- js.html.idb.VersionChangeRequest
    - Obsolete.
- js.html.rtc.DataChannelEvent
    - Obsolete.
- js.html.rtc.IceCandidateEvent
    - Obsolete.
- js.html.rtc.LocalMediaStream
    - Obsolete.
- js.html.rtc.MediaStream
    - Obsolete.
- js.html.rtc.MediaStreamEvent
    - Obsolete.
- js.html.rtc.MediaStreamList
    - Obsolete.
- js.html.rtc.MediaStreamTrack
    - Obsolete.
- js.html.rtc.MediaStreamTrackEvent
    - Obsolete.
- js.html.rtc.MediaStreamTrackList
    - Obsolete.
- js.html.rtc.NavigatorUserMediaError
    - Obsolete.
- js.html.rtc.StatsElement
    - Obsolete.
- js.html.rtc.StatsResponse
    - Obsolete.
- js.html.sql.Database
    - Obsolete.
- js.html.sql.DatabaseSync
    - Obsolete.
- js.html.sql.Error
    - Obsolete.
- js.html.sql.Exception
    - Obsolete.
- js.html.sql.ResultSet
    - Obsolete.
- js.html.sql.ResultSetRowList
    - Obsolete.
- js.html.sql.Transaction
    - Obsolete.
- js.html.sql.TransactionSync
    - Obsolete.
- js.html.svg.AltGlyphDefElement
    - ?
- js.html.svg.AltGlyphItemElement
    - ?
- js.html.svg.AnimateColorElement
    - ?
- js.html.svg.Color
    - ?
- js.html.svg.CursorElement
    - ?
- js.html.svg.ElementInstance
    - ?
- js.html.svg.ElementInstanceList
    - ?
- js.html.svg.Exception
    - ?
- js.html.svg.ExternalResourcesRequired
    - ?
- js.html.svg.FilterPrimitiveStandardAttributes
    - ?
- js.html.svg.FitToViewBox
    - ?
- js.html.svg.FontElement
    - ?
- js.html.svg.FontFaceElement
    - ?
- js.html.svg.FontFaceFormatElement
    - ?
- js.html.svg.FontFaceNameElement
    - ?
- js.html.svg.FontFaceSrcElement
    - ?
- js.html.svg.FontFaceUriElement
    - ?
- js.html.svg.GlyphElement
    - ?
- js.html.svg.GlyphRefElement
    - ?
- js.html.svg.HKernElement
    - ?
- js.html.svg.LangSpace
    - ?
- js.html.svg.Locatable
    - ?
- js.html.svg.MissingGlyphElement
    - ?
- js.html.svg.Paint
    - ?
- js.html.svg.RenderingIntent
    - ?
- js.html.svg.Stylable
    - ?
- js.html.svg.TRefElement
    - ?
- js.html.svg.Tests
    - ?
- js.html.svg.Transformable
    - ?
- js.html.svg.URIReference
    - ?
- js.html.svg.VKernElement
    - ?
- js.html.svg.ViewSpec
    - ?
- js.html.webgl.CompressedTextureS3TC
    - Renamed to ExtensionCompressedTextureS3TC.
- js.html.webgl.DebugRendererInfo
    - Renamed to ExtensionDebugRendererInfo.
- js.html.webgl.DebugShaders
    - Renamed to ExtensionDebugShaders.
- js.html.webgl.DepthTexture
    - Renamed to ExtensionDepthTexture.
- js.html.webgl.EXTTextureFilterAnisotropic
    - Renamed to ExtensionTextureFilterAnisotropic.
- js.html.webgl.LoseContext
    - Renamed to ExtensionLoseContext.
- js.html.webgl.OESElementIndexUint
    - Obsolete.
- js.html.webgl.OESStandardDerivatives
    - Renamed to ExtensionStandardDerivatives.
- js.html.webgl.OESTextureFloat
    - Renamed to ExtensionTextureFloat.
- js.html.webgl.OESVertexArrayObject
    - Renamed to ExtensionVertexArrayObject.
- js.html.webgl.VertexArrayObjectOES
    - Renamed to VertexArray.

## Regarding HtmlElement and HTMLElement

In Haxe 3.1, js.html.Element was a unified version of Element and HTMLElement. Our Element contained functionality from both Element and HTMLElement.

In Haxe 3.2, we match the DOM spec more closely. There's a js.html.HTMLElement now, and you probably want to use it instead of Element (unless you're working with SVG or something). That required renaming js.html.HtmlElement to HTMLHtmlElement.

Haxe 3.1:
* Element
* HtmlElement

Haxe 3.2:
* Element
* HTMLElement
* HTMLHtmlElement
