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
ms.openlocfilehash: d32c0860f76aeeaa64a060a55579d05c1eb571ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478182"
---
# <a name="dbenginedefaulttype-property-dao"></a>DBEngine.DefaultType プロパティ (DAO)


**適用されます**Access 2013 |。Office 2013

次に作成される **[Workspace](workspace-object-dao.md)** オブジェクトが使用するワークスペースの種類を示す値を設定または取得します。

## <a name="syntax"></a>構文

*式*です。DefaultType

*式***DBEngine**オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

設定値または戻り値は、 **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** クラスの定数のいずれかです。


> [!NOTE]
> <P>[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</P>



**[CreateWorkspace](dbengine-createworkspace-method-dao.md)** メソッドに型引数を設定することによって、1 つの**ワークスペース**の設定をオーバーライドできます。

