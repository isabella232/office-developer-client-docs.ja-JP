---
title: Append メソッド (ADOX Groups)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76c602896a629881d06a3f3cf80326e02340186e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479255"
---
# <a name="append-method-adox-groups"></a>Append メソッド (ADOX Groups)


**適用されます**Access 2013 |。Office 2013



新しい [Group](group-object-adox.md) オブジェクトを [Groups](groups-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*グループ*です。*グループ*を追加します。

## <a name="parameters"></a>パラメーター

  - *Group*

  - 追加する **Group** オブジェクトを指定します。または、新たに作成して追加するグループの名前を指定します。

## <a name="remarks"></a>解説

**Catalog** の [Groups](catalog-object-adox.md) コレクションは、そのカタログのすべてのグループ アカウントを表します。 **User** の [Groups](user-object-adox.md) コレクションは、ユーザーが属するグループのみを表します。

プロバイダーがグループの作成をサポートしていない場合は、エラーが発生します。


> [!NOTE]
> <P>[!メモ] <STRONG>Group</STRONG> オブジェクトを <STRONG>User</STRONG> オブジェクトの <STRONG>Groups</STRONG> コレクションに追加する前に、追加するものと同じ <STRONG>Name プロパティ (ADOX)</STRONG> を持つ <A href="name-property-adox.md">Group</A> オブジェクトが、あらかじめ <STRONG>Catalog</STRONG> の <STRONG>Groups</STRONG> コレクションに存在している必要があります。</P>


