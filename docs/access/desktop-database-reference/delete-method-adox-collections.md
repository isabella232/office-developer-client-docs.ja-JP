---
title: Delete メソッド (ADOX コレクション)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 54c67848d321125af44d9f5bf50f3aa582b043bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294079"
---
# <a name="delete-method-adox-collections"></a>Delete メソッド (ADOX コレクション)

**適用先:** Access 2013、Office 2013

コレクションからオブジェクトを削除します。

## <a name="syntax"></a>構文

*コレクション*。*名前*の削除

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Name* |削除するオブジェクトの名前または位置 (インデックス) を示すバリアント型 ( **Variant** ) を指定します。|

## <a name="remarks"></a>注釈

コレクションに *Name* が存在していない場合は、エラーが発生します。

[Tables](tables-collection-adox.md) コレクションおよび [Users](users-collection-adox.md) コレクションでは、プロバイダーがテーブルやユーザーの削除をサポートしていない場合、それぞれエラーが発生します。[Procedures](procedures-collection-adox.md) コレクションおよび [Views](views-collection-adox.md) コレクションでは、プロバイダーが持続的なコマンドをサポートしていない場合、**Delete** は失敗します。

