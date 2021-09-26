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
ms.localizationpriority: medium
ms.openlocfilehash: 619d46e493f45745d47a9bb8188df8dfe240c3ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59632078"
---
# <a name="dbenginedefaulttype-property-dao"></a>DBEngine.DefaultType プロパティ (DAO)


**適用先**: Access 2013、Office 2013

次に作成される **[Workspace](workspace-object-dao.md)** オブジェクトが使用するワークスペースの種類を示す値を設定または取得します。

## <a name="syntax"></a>構文

*式* .DefaultType

*式* **DBEngine** オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

設定値または戻り値は、 **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** クラスの定数のいずれかです。


> [!NOTE]
> [!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。

引数 type を CreateWorkspace メソッドに設定することで、1 つの **Workspace** の設定 **[を上書き](dbengine-createworkspace-method-dao.md)** できます。

