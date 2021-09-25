---
title: Number プロパティ (ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 6707072a61f6be3538e8c0365383584802858981
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597171"
---
# <a name="number-property-ado"></a>Number プロパティ (ADO)


**適用先**: Access 2013、Office 2013

[Error](error-object-ado.md) オブジェクトを一意に識別する数値を示します。

## <a name="return-value"></a>戻り値

[ErrorValueEnum](errorvalueenum.md) 定数のいずれかに対応する長整数型 (**Long**) の値を返します。

## <a name="remarks"></a>注釈

**Number** プロパティは、発生したエラーを調べるために使用します。プロパティの値は、エラー条件に対応した一意な数値です。

The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259). These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself. これらの番号の詳細については、「OLE DB プログラマ リファレンス」の第 16 章 *を参照してください。*

