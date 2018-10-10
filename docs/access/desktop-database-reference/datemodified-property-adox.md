---
title: DateModified プロパティ (ADOX)
TOCTitle: DateModified Property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8465f97565d8519196b8221089121670ceedb275
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476541"
---
# <a name="datemodified-property-adox"></a>DateModified プロパティ (ADOX)


**適用されます**Access 2013 |。Office 2013

オブジェクトが最後に変更された日付を示します。

## <a name="return-values"></a>戻り値

変更された日付を示すバリアント型 ( **Variant** ) の値を返します。プロバイダーが **DateModified** をサポートしていない場合、値は Null 値になります。

## <a name="remarks"></a>解説

新しく追加されたオブジェクトの **DateModified** プロパティは Null 値です。新しい [View](view-object-adox.md) または [Procedure](procedure-object-adox.md) を追加した後に、 [DateModified](refresh-method-ado.md) プロパティの値を取得するには、 [Views](views-collection-adox.md) コレクションまたは [Procedures](procedures-collection-adox.md) コレクションの **Refresh** メソッドを呼び出す必要があります。

