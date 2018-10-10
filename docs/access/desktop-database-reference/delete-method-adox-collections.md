---
title: Delete メソッド (ADOX コレクション)
TOCTitle: Delete Method (ADOX Collections)
ms:assetid: bcf9b8dd-cc7a-c1f9-fd93-58694766c4d9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249909(v=office.15)
ms:contentKeyID: 48547423
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ea02f02270649783873f1f086bb9f39b804034a2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479136"
---
# <a name="delete-method-adox-collections"></a>Delete メソッド (ADOX コレクション)


**適用されます**Access 2013 |。Office 2013



コレクションからオブジェクトを削除します。

## <a name="syntax"></a>構文

*コレクション*です。*名前*を削除します。

## <a name="parameters"></a>パラメーター

  - *Name*

  - 削除するオブジェクトの名前または位置 (インデックス) を示すバリアント型 ( **Variant** ) を指定します。

## <a name="remarks"></a>解説

*名*がコレクション内に存在しない場合は、エラーが発生します。

[Tables](tables-collection-adox.md) コレクションおよび [Users](users-collection-adox.md) コレクションでは、プロバイダーがテーブルやユーザーの削除をサポートしていない場合、それぞれエラーが発生します。 [Procedures](procedures-collection-adox.md) コレクションおよび [Views](views-collection-adox.md) コレクションでは、プロバイダーが持続的なコマンドをサポートしていない場合、 **Delete** は失敗します。

