---
title: Delete メソッド (ADOX コレクション)
TOCTitle: Delete method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0e1790f8ec28343f04b86c5e4b0f0f5bfd903a18
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594336"
---
# <a name="delete-method-adox-collections"></a>Delete メソッド (ADOX コレクション)

**適用先**: Access 2013、Office 2013

コレクションからオブジェクトを削除します。

## <a name="syntax"></a>構文

*コレクション*.名前の *削除*

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*名前* |削除するオブジェクトの名前または位置 (インデックス) を示すバリアント型 ( **Variant** ) を指定します。|

## <a name="remarks"></a>注釈

コレクションに *Name* が存在していない場合は、エラーが発生します。

[Tables](tables-collection-adox.md) コレクションおよび [Users](users-collection-adox.md) コレクションでは、プロバイダーがテーブルやユーザーの削除をサポートしていない場合、それぞれエラーが発生します。[Procedures](procedures-collection-adox.md) コレクションおよび [Views](views-collection-adox.md) コレクションでは、プロバイダーが持続的なコマンドをサポートしていない場合、**Delete** は失敗します。

