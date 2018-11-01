---
title: DefinedSize プロパティ (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0a0e67cfdbe60ebf2c49cb3e726311d2fa61bd3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868855"
---
# <a name="definedsize-property-ado"></a>DefinedSize プロパティ (ADO)


**適用されます**Access 2013、Office 2013。

[Field](field-object-ado.md) オブジェクトのデータ容量を示します。

## <a name="return-value"></a>戻り値

バイト数でフィールドの定義サイズを反映する長整数型 ( **Long** ) の値を返します。

## <a name="remarks"></a>解説

**DefinedSize** プロパティは、 **Field** オブジェクトのデータ容量を調べるために使います。

**DefinedSize** プロパティと [ActualSize](actualsize-property-ado.md) プロパティは異なるものです。たとえば、宣言タイプが **adVarChar** で **DefinedSize** プロパティ値が 50 の、1 文字を格納した **Field** オブジェクトがあるとします。このオブジェクトが返す **ActualSize** プロパティ値は、1 文字をバイト数で表した長さです。

