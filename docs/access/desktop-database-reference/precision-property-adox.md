---
title: Precision プロパティ (ADOX)
TOCTitle: Precision property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fe859810252376024ebaa327a9203309d4bb8cd7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622117"
---
# <a name="precision-property-adox"></a>Precision プロパティ (ADOX)


**適用先**: Access 2013、Office 2013

列のデータ値の最大桁数を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

**Type** プロパティが数値型の場合に、列のデータ値の最大桁数を表す長整数型 ( [Long](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-columnadox) ) の値を設定および取得します。数値型以外のデータ型の場合、 **Precision** プロパティは無視されます。

## <a name="remarks"></a>注釈

既定値はゼロ (0) です。

このプロパティは、[Column](column-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。

