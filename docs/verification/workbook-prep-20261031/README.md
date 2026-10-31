# Workbook and Prep live verification, 2026-10-31

These images show the actual disposable Tableau Cloud flow used for Issues #1167, #1168 and #1169. Every visible owner name is covered with an opaque black rectangle. Only masked images were saved, and each image was visually reviewed.

The source-pinned MCP runtime successfully published and downloaded the TFLX flow. Downloaded bytes matched an independent REST download (960205 bytes; SHA256 da32a2ba0a0896f62f6a25e9878e5689467293e91df605c9fdeff6e175e4f3e6).

The move-flow runtime at f8427081cfd4046303ce8c580e9eb232a6011b6b (runtime SHA256 9a9700413edf1bc0c93ae40be36d984ecfd85f6e6c1f85f15c69f9cb98a18f03) moved the flow to the disposable destination project and restored it to the source project. Independent REST readback confirmed both project changes and unchanged ownership.

The TFL publication image shows the second disposable flow. Its server download was returned as TFLX, and the verification adapter stopped at its original-extension requirement before the independent byte comparison. This is not claimed as a completed native TFL download test.

The workbook past-revision download and the connection endpoint change remain unverified. The database fixture publish returned HTTP 400. No flow was executed. Both session-owned flows and both empty projects were removed after capture; credentials were disposed.

Screenshots support the MCP/readback evidence; they do not independently prove an MCP write. Upstream CI and peer approval remain pending.
