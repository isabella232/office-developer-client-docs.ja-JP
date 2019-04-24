---
title: Append メソッド (ADOX Groups)
TOCTitle: Append method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f0e7731777e3d82e3746c3886bdbddb3e43db66
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297103"
---
# <a name="append-method-adox-groups"></a>Append メソッド (ADOX Groups)

**適用先:** Access 2013、Office 2013

新しい [Group](group-object-adox.md) オブジェクトを [Groups](groups-collection-adox.md) コレクションに追加します。

## <a name="syntax"></a>構文

*グループ*。*グループ*の追加

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Group* |追加する **Group** オブジェクトを指定します。または、新たに作成して追加するグループの名前を指定します。|

## <a name="remarks"></a>注釈

**Catalog** の [Groups](catalog-object-adox.md) コレクションは、そのカタログのすべてのグループ アカウントを表します。 **User** の [Groups](user-object-adox.md) コレクションは、ユーザーが属するグループのみを表します。

プロバイダーがグループの作成をサポートしていない場合は、エラーが発生します。

> [!NOTE]
> [!メモ] **Group** オブジェクトを **User** オブジェクトの **Groups** コレクションに追加する前に、追加するものと同じ **Name プロパティ (ADOX)** を持つ [Group](name-property-adox.md) オブジェクトが、あらかじめ **Catalog** の **Groups** コレクションに存在している必要があります。


