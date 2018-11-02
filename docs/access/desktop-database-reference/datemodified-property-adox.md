---
title: DateModified プロパティ (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 447b7c609dd122d825d97a7430349eb88f8f7b0b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923953"
---
# <a name="datemodified-property-adox"></a>DateModified プロパティ (ADOX)


**適用されます**Access 2013、Office 2013。

オブジェクトが最後に変更された日付を示します。

## <a name="return-values"></a>戻り値

変更された日付を示すバリアント型 ( **Variant** ) の値を返します。プロバイダーが **DateModified** をサポートしていない場合、値は Null 値になります。

## <a name="remarks"></a>解説

新しく追加されたオブジェクトの **DateModified** プロパティは Null 値です。新しい [View](view-object-adox.md) または [Procedure](procedure-object-adox.md) を追加した後に、 [DateModified](refresh-method-ado.md) プロパティの値を取得するには、 [Views](views-collection-adox.md) コレクションまたは [Procedures](procedures-collection-adox.md) コレクションの **Refresh** メソッドを呼び出す必要があります。

