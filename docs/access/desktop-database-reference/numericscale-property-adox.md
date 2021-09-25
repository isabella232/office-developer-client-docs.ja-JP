---
title: NumericScale プロパティ (ADOX)
TOCTitle: NumericScale property (ADOX)
ms:assetid: ebe73bdc-2570-f54a-3d2f-85a2a4634c9a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250197(v=office.15)
ms:contentKeyID: 48548501
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 17cc0a52a138cf1d16904fc1b7b2bd907a79aba8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615187"
---
# <a name="numericscale-property-adox"></a>NumericScale プロパティ (ADOX)


**適用先**: Access 2013、Office 2013

列中の数値の小数点以下の桁数を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

**Type** プロパティが [adNumeric](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) または **adDecimal** の場合、列にあるデータ値の小数点以下の桁数をバイト型 ( **Byte** ) の値で設定および取得します。その他のすべてのデータ型では、 **NumericScale** は無視されます。

## <a name="remarks"></a>注釈

既定値は 0 (ゼロ) です。

**NumericScale** は、 [Column](column-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。

