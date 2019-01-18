---
title: Name プロパティ (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c7021c6f97d1aaa9c82e65eab98a3259d6eb87e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707984"
---
# <a name="name-property-adox"></a>Name プロパティ (ADOX)

**適用されます**Access 2013、Office 2013。

オブジェクトの名前を示します。

## <a name="settings-and-return-values"></a>設定値および戻り値

文字列型 ( **String** ) の値を設定または取得します。

## <a name="remarks"></a>解説

名前は、コレクション内で一意である必要はありません。

**Name** プロパティは、 [Column](column-object-adox.md)、[Group](group-object-adox.md)、[Key](key-object-adox.md)、[Index](index-object-adox.md)、[Table](table-object-adox.md)、および [User](user-object-adox.md) オブジェクトでは、値の取得および設定が可能です。 **Name** プロパティは、 [Catalog](catalog-object-adox.md)、[Procedure](procedure-object-adox.md)、および [View](view-object-adox.md) オブジェクトでは、値の取得のみ可能です。

値の取得および設定が可能なオブジェクト (**Column**、**Group**、**Key**、**Index**、**Table**、および **User** オブジェクト) では、既定値は空の文字列 ("") です。

> [!NOTE]
> - [!メモ] キーの場合、このプロパティは、既にコレクションに追加されている **Key** オブジェクトでは値の取得のみ可能です。
> - [!メモ] テーブルの場合、このプロパティは、既にコレクションに追加されている **Table** オブジェクトでは値の取得のみ可能です。


