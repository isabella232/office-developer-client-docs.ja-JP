---
title: DateModified プロパティ (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0ed5b0078c934f6aa47422f261b77df248ba4042
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585852"
---
# <a name="datemodified-property-adox"></a>DateModified プロパティ (ADOX)


**適用先**: Access 2013、Office 2013

オブジェクトが最後に変更された日付を示します。

## <a name="return-values"></a>戻り値

変更された日付を示すバリアント型 ( **Variant** ) の値を返します。プロバイダーが **DateModified** をサポートしていない場合、値は Null 値になります。

## <a name="remarks"></a>注釈

新しく追加されたオブジェクトの **DateModified** プロパティは Null 値です。新しい [View](view-object-adox.md) または [Procedure](procedure-object-adox.md) を追加した後に、**DateModified** プロパティの値を取得するには、[Views](views-collection-adox.md) コレクションまたは [Procedures](procedures-collection-adox.md) コレクションの [Refresh](refresh-method-ado.md) メソッドを呼び出す必要があります。

