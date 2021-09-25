---
title: Name プロパティ (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f067c16c2c7d8d584d6900bff6212b469c3b7fe4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602200"
---
# <a name="name-property-adox"></a>Name プロパティ (ADOX)

**適用先**: Access 2013、Office 2013

オブジェクトの名前を示します。

## <a name="settings-and-return-values"></a>設定および戻り値

文字列型 (**String**) の値を設定または取得します。

## <a name="remarks"></a>注釈

名前は、コレクション内で一意である必要はありません。

**Name** プロパティは、 [Column](column-object-adox.md)、[Group](group-object-adox.md)、[Key](key-object-adox.md)、[Index](index-object-adox.md)、[Table](table-object-adox.md)、および [User](user-object-adox.md) オブジェクトでは、値の取得および設定が可能です。 **Name** プロパティは、 [Catalog](catalog-object-adox.md)、[Procedure](procedure-object-adox.md)、および [View](view-object-adox.md) オブジェクトでは、値の取得のみ可能です。

値の取得および設定が可能なオブジェクト (**Column**、**Group**、**Key**、**Index**、**Table**、および **User** オブジェクト) では、既定値は空の文字列 ("") です。

> [!NOTE]
> - キーの場合、このプロパティは、既にコレクションに追加されている **Key** オブジェクトでは値の取得のみ可能です。
> - [!メモ] テーブルの場合、このプロパティは、既にコレクションに追加されている **Table** オブジェクトでは値の取得のみ可能です。


