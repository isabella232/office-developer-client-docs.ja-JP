---
title: DateCreated プロパティ (ADOX)
TOCTitle: DateCreated property (ADOX)
ms:assetid: ee975bf5-7d44-a993-d1c0-077993515698
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250209(v=office.15)
ms:contentKeyID: 48548564
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4a7df2a0b4d348402560c6781af80f56f55ecb9d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585866"
---
# <a name="datecreated-property-adox"></a>DateCreated プロパティ (ADOX)


**適用先**: Access 2013、Office 2013

オブジェクトが作成された日付を示します。

## <a name="return-values"></a>戻り値

作成された日付を示すバリアント型 ( **Variant** ) の値を返します。プロバイダーが **DateCreated** をサポートしていない場合、値は Null 値になります。

## <a name="remarks"></a>注釈

新しく追加されたオブジェクトの **DateCreated** プロパティは Null 値です。新しい [View](view-object-adox.md) または [Procedure](procedure-object-adox.md) を追加した後に、**DateCreated** プロパティの値を取得するには、[Views](views-collection-adox.md) コレクションまたは [Procedures](procedures-collection-adox.md) コレクションの [Refresh](refresh-method-ado.md) メソッドを呼び出す必要があります。

