---
title: Append メソッド (ADOX Groups)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 8e8aab9b70fc418c471599885e4061bfd7762176
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607361"
---
# <a name="append-method-adox-groups"></a>Append メソッド (ADOX Groups)

**適用先**: Access 2013、Office 2013

新しい [Group](group-object-adox.md) オブジェクトを [Groups](groups-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*グループ*。グループの *追加*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Group* |追加する **Group** オブジェクトを指定します。または、新たに作成して追加するグループの名前を指定します。|

## <a name="remarks"></a>注釈

**Catalog** の [Groups](catalog-object-adox.md) コレクションは、そのカタログのすべてのグループ アカウントを表します。 **User** の [Groups](user-object-adox.md) コレクションは、ユーザーが属するグループのみを表します。

プロバイダーがグループの作成をサポートしていない場合は、エラーが発生します。

> [!NOTE]
> [!メモ] **Group** オブジェクトを **User** オブジェクトの **Groups** コレクションに追加する前に、追加するものと同じ **Name プロパティ (ADOX)** を持つ [Group](name-property-adox.md) オブジェクトが、あらかじめ **Catalog** の **Groups** コレクションに存在している必要があります。


