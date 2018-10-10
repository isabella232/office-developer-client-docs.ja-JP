---
title: Precision プロパティ (ADOX)
TOCTitle: Precision Property (ADOX)
ms:assetid: 5d8ca497-572a-52e0-18aa-f82deaea0813
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249330(v=office.15)
ms:contentKeyID: 48545117
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5fab2a7dc7a2d9f05e22b064acfaeabf93106a3e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476625"
---
# <a name="precision-property-adox"></a>Precision プロパティ (ADOX)


**適用されます**Access 2013 |。Office 2013

列のデータ値の最大桁数を示します。

## <a name="settings-and-return-values"></a>設定値と戻り値

**Type** プロパティが数値型の場合に、列のデータ値の最大桁数を表す長整数型 ( [Long](https://msdn.microsoft.com/library/jj249169\(v=office.15\)) ) の値を設定および取得します。数値型以外のデータ型の場合、 **Precision** プロパティは無視されます。

## <a name="remarks"></a>解説

既定値は 0 (ゼロ) です。

このプロパティは、[Column](column-object-adox.md) オブジェクトが既にコレクションに追加されている場合、値の取得のみが可能になります。

