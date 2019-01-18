---
title: DBEngine.DefaultType プロパティ (DAO)
TOCTitle: DefaultType Property
ms:assetid: b4371f3e-1ce0-1d0f-93a8-0c5329b510ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822060(v=office.15)
ms:contentKeyID: 48547217
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053580
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 23f6c87ede6da2cc5b2f3203bfa13cb17bf93e82
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713591"
---
# <a name="dbenginedefaulttype-property-dao"></a>DBEngine.DefaultType プロパティ (DAO)


**適用されます**Access 2013、Office 2013。

次に作成される **[Workspace](workspace-object-dao.md)** オブジェクトが使用するワークスペースの種類を示す値を設定または取得します。

## <a name="syntax"></a>構文

*式*です。DefaultType

*式***DBEngine**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

設定値または戻り値は、 **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** クラスの定数のいずれかです。


> [!NOTE]
> [!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。

**[CreateWorkspace](dbengine-createworkspace-method-dao.md)** メソッドに型引数を設定することによって、1 つの**ワークスペース**の設定をオーバーライドできます。

