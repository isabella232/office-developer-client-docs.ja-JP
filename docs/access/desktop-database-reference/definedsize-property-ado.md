---
title: DefinedSize プロパティ (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 121e81734fc5ecc0a761dae53942f1cbed98df2a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715327"
---
# <a name="definedsize-property-ado"></a>DefinedSize プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Field](field-object-ado.md) オブジェクトのデータ容量を示します。

## <a name="return-value"></a>戻り値

バイト数でフィールドの定義サイズを反映する長整数型 ( **Long** ) の値を返します。

## <a name="remarks"></a>解説

**DefinedSize** プロパティは、 **Field** オブジェクトのデータ容量を調べるために使います。

**DefinedSize** プロパティと [ActualSize](actualsize-property-ado.md) プロパティは異なるものです。たとえば、宣言タイプが **adVarChar** で **DefinedSize** プロパティ値が 50 の、1 文字を格納した **Field** オブジェクトがあるとします。このオブジェクトが返す **ActualSize** プロパティ値は、1 文字をバイト数で表した長さです。

