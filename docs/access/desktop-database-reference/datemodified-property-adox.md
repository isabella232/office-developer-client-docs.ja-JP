---
title: DateModified プロパティ (ADOX)
TOCTitle: DateModified property (ADOX)
ms:assetid: aebe8818-82e7-84a4-24d7-d97afa32e193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249827(v=office.15)
ms:contentKeyID: 48547078
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: daf72804d51c18b5875e607ce5fdb0dfe20f406c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294408"
---
# <a name="datemodified-property-adox"></a>DateModified プロパティ (ADOX)


**適用先:** Access 2013、Office 2013

オブジェクトが最後に変更された日付を示します。

## <a name="return-values"></a>戻り値

変更された日付を示すバリアント型 ( **Variant** ) の値を返します。 プロバイダーが **DateModified** をサポートしていない場合、値は Null 値になります。

## <a name="remarks"></a>注釈

新しく追加されたオブジェクトの **DateModified** プロパティは Null 値です。新しい [View](view-object-adox.md) または [Procedure](procedure-object-adox.md) を追加した後に、**DateModified** プロパティの値を取得するには、[Views](views-collection-adox.md) コレクションまたは [Procedures](procedures-collection-adox.md) コレクションの [Refresh](refresh-method-ado.md) メソッドを呼び出す必要があります。

