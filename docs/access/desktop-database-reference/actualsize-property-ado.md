---
title: ActualSize プロパティ (ADO)
TOCTitle: ActualSize Property (ADO)
ms:assetid: 020a414d-e6aa-5fb9-9b77-bd9d10124f8a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248787(v=office.15)
ms:contentKeyID: 48542949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d0fa7b4f5fe27c25db51338dd1dfd1a68a936364
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476215"
---
# <a name="actualsize-property-ado"></a>ActualSize プロパティ (ADO)

**適用されます**Access 2013 |。Office 2013

フィールドの値の実際の長さを示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

長整数型 ( **Long** ) の値を返します。プロバイダーによっては、このプロパティを BLOB データの予約空間に設定することができる場合もあり、この場合の既定値は 0 です。

## <a name="remarks"></a>解説

**ActualSize** プロパティを使用すると、 [Field](field-object-ado.md) オブジェクトの値の実際の長さを取得できます。どのフィールドについても、 **ActualSize** プロパティは値の取得のみ可能です。ADO が **Field** オブジェクトの値の長さを判断できない場合は、 **ActualSize** プロパティからは **adUnknown** が返されます。

次の具体例で示すように、 **ActualSize** プロパティと [DefinedSize](definedsize-property-ado.md) プロパティは異なります。 **adVarChar** 型で宣言された **Field** オブジェクトで最大長が 50 文字の場合、 **DefinedSize** プロパティは 50 という値を返しますが、 **ActualSize** プロパティは、カレント レコードのそのフィールドに格納されているデータの長さを返します。255 バイトより大きい **DefinedSize** を持つ **Fields** は、可変長列として扱われます。

