---
title: DBEngine の type プロパティ (DAO)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294380"
---
# <a name="dbenginedefaulttype-property-dao"></a><span data-ttu-id="d236e-102">DBEngine の type プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="d236e-102">DBEngine.DefaultType property (DAO)</span></span>


<span data-ttu-id="d236e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d236e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d236e-104">次に作成される **[Workspace](workspace-object-dao.md)** オブジェクトが使用するワークスペースの種類を示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="d236e-104">Sets or returns a value that indicates what type of workspace will be used by the next **[Workspace](workspace-object-dao.md)** object created.</span></span>

## <a name="syntax"></a><span data-ttu-id="d236e-105">構文</span><span class="sxs-lookup"><span data-stu-id="d236e-105">Syntax</span></span>

<span data-ttu-id="d236e-106">*式*。DefaultType</span><span class="sxs-lookup"><span data-stu-id="d236e-106">*expression* .DefaultType</span></span>

<span data-ttu-id="d236e-107">\*式\***DBEngine**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d236e-107">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d236e-108">注釈</span><span class="sxs-lookup"><span data-stu-id="d236e-108">Remarks</span></span>

<span data-ttu-id="d236e-109">設定値または戻り値は、 **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** クラスの定数のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="d236e-109">The setting or return value can be one of the of the **[WorkspaceTypeEnum](workspacetypeenum-enumeration-dao.md)** constants.</span></span>


> [!NOTE]
> <span data-ttu-id="d236e-p101">[!メモ] Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="d236e-p101">ODBCDirect workspaces are not supported in Microsoft Access 2013. Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>

<span data-ttu-id="d236e-112">引数 type を**[createworkspace](dbengine-createworkspace-method-dao.md)** メソッドに設定することにより、1つの**ワークスペース**に対して設定をオーバーライドできます。</span><span class="sxs-lookup"><span data-stu-id="d236e-112">The setting can be overridden for a single **Workspace** by setting the type argument to the **[CreateWorkspace](dbengine-createworkspace-method-dao.md)** method.</span></span>

