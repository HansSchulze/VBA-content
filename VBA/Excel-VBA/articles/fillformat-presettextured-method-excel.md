---
title: FillFormat.PresetTextured Method (Excel)
keywords: vbaxl10.chm115006
f1_keywords:
- vbaxl10.chm115006
ms.prod: excel
api_name:
- Excel.FillFormat.PresetTextured
ms.assetid: 44661e53-9aee-7abd-6a6e-b6cb0a97ee2d
ms.date: 06/08/2017
---


# FillFormat.PresetTextured Method (Excel)

Sets the specified fill format to a preset texture.


## Syntax

 _expression_ . **PresetTextured**( **_PresetTexture_** )

 _expression_ A variable that represents a **FillFormat** object.


### Parameters



|**Name**|**Required/Optional**|**Data Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _PresetTexture_|Required| **[MsoPresetTexture](http://msdn.microsoft.com/library/fbbc897d-f5db-eb0d-20d9-f6b7e9bbcf4f%28Office.15%29.aspx)**|The type of texture to apply.|

## Example

This example sets the fill format for chart two to the same style used for chart one.


```vb
Set c1f = Charts(1).ChartArea.Fill 
If c1f.Type = msoFillTextured Then 
    With Charts(2).ChartArea.Fill 
        .Visible = True 
        If c1f.TextureType = msoTexturePreset Then 
            .PresetTextured c1f.PresetTexture 
        Else 
            .UserTextured c1f.TextureName 
        End If 
    End With 
End If
```


## See also


#### Concepts


[FillFormat Object](fillformat-object-excel.md)

