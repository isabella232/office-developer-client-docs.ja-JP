---
title: Name プロパティ (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a65bad49c7b9b7a7af91403b1119923b62daa04a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931247"
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
> <P>[!メモ] キーの場合、このプロパティは、既にコレクションに追加されている <STRONG>Key</STRONG> オブジェクトでは値の取得のみ可能です。</P>




> [!NOTE]
> <P>[!メモ] テーブルの場合、このプロパティは、既にコレクションに追加されている <STRONG>Table</STRONG> オブジェクトでは値の取得のみ可能です。</P>


