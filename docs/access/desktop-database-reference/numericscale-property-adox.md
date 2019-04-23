---
title: numericscale プロパティ (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d706bad7d1f605933a951498705657c3c454a2d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288519"
---
# <a name="numericscale-property-adox"></a>numericscale プロパティ (ADOX)


**適用先:** Access 2013、Office 2013

列中の数値の小数点以下の桁数を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

**Type** プロパティが [adNumeric](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) または **adDecimal** の場合、列にあるデータ値の小数点以下の桁数をバイト型 ( **Byte** ) の値で設定および取得します。その他のすべてのデータ型では、 **NumericScale** は無視されます。

## <a name="remarks"></a>注釈

既定値は 0 (ゼロ) です。

**NumericScale** は、 [Column](column-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。

