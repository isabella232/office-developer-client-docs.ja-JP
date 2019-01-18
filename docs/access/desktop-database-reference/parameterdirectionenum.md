---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fac07165416841691ee7bc3ca5dfcdc366861023
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715502"
---
# <a name="parameterdirectionenum"></a>ParameterDirectionEnum


**適用されます**Access 2013、Office 2013。

[Parameter](parameter-object-ado.md) が入力パラメーターと出力パラメーターのいずれか、またはその両方を表すのか、あるいはストアド プロシージャからの戻り値であるかを表します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adParamInput</strong></p></td>
<td><p>1</p></td>
<td><p>既定値。パラメーターが入力パラメーターを表すことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adParamInputOutput</strong></p></td>
<td><p>3</p></td>
<td><p>パラメーターが入力パラメーターと出力パラメーターの両方を表すことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adParamOutput</strong></p></td>
<td><p>2</p></td>
<td><p>パラメーターが出力パラメーターを表すことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adParamReturnValue</strong></p></td>
<td><p>4</p></td>
<td><p>パラメーターが戻り値を表すことを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adParamUnknown</strong></p></td>
<td><p>0</p></td>
<td><p>パラメーターの方向が不明であることを示します。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC に相当

パッケージ: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.ParameterDirection.INPUT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ParameterDirection.INPUTOUTPUT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ParameterDirection.OUTPUT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ParameterDirection.RETURNVALUE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ParameterDirection.UNKNOWN</p></td>
</tr>
</tbody>
</table>

