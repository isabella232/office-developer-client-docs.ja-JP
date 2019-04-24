---
title: 未定義の size プロパティ (ADO)
TOCTitle: DefinedSize property (ADO)
ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15)
ms:contentKeyID: 48546257
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 121e81734fc5ecc0a761dae53942f1cbed98df2a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294135"
---
# <a name="definedsize-property-ado"></a>未定義の size プロパティ (ADO)


**適用先:** Access 2013、Office 2013

[Field](field-object-ado.md) オブジェクトのデータ容量を示します。

## <a name="return-value"></a>戻り値

バイト数でフィールドの定義サイズを反映する長整数型 (**Long**) の値を返します。

## <a name="remarks"></a>注釈

**DefinedSize** プロパティは、**Field** オブジェクトのデータ容量を調べるために使います。

**DefinedSize** プロパティと [ActualSize](actualsize-property-ado.md) プロパティは異なるものです。たとえば、宣言タイプが **adVarChar** で **DefinedSize** プロパティ値が 50 の、1 文字を格納した **Field** オブジェクトがあるとします。このオブジェクトが返す **ActualSize** プロパティ値は、1 文字をバイト数で表した長さです。

