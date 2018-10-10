---
title: Connect プロパティ (RDS)
TOCTitle: Connect Property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb628356e4d93201c38cf84a9c3245b13e044ee3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478950"
---
# <a name="connect-property-rds"></a><span data-ttu-id="772f9-102">Connect プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="772f9-102">Connect Property (RDS)</span></span>


<span data-ttu-id="772f9-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="772f9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="772f9-104">クエリおよび更新操作が実行されるデータベース名を示します。</span><span class="sxs-lookup"><span data-stu-id="772f9-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="772f9-105">**Connect** プロパティは、デザイン時に [RDS.DataControl](datacontrol-object-rds.md) オブジェクトの OBJECT タグ内で、または実行時にスクリプト コード (たとえば、VBScript) 内で設定できます。</span><span class="sxs-lookup"><span data-stu-id="772f9-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="772f9-106">構文</span><span class="sxs-lookup"><span data-stu-id="772f9-106">Syntax</span></span>

<span data-ttu-id="772f9-107">デザイン時:\<パラメーターの名前 [接続] の値を = =「接続文字列」\></span><span class="sxs-lookup"><span data-stu-id="772f9-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="772f9-108">実行時間: DataControl.Connect =「接続文字列」</span><span class="sxs-lookup"><span data-stu-id="772f9-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="772f9-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="772f9-109">Parameters</span></span>

  - <span data-ttu-id="772f9-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="772f9-110">*ConnectionString*</span></span>

  - <span data-ttu-id="772f9-p101">有効な接続文字列を指定します。接続文字列全般の説明については、[ConnectionString](connectionstring-property-ado.md) プロパティかプロバイダーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="772f9-p101">A valid connection string. For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="772f9-p102">[!メモ] <STRONG>RDS.DataControl</STRONG> のプロバイダーとして MS Remote を指定すると、4 層のシナリオが作成されます。3 層を超えるシナリオについては未確認なので避けてください。</span><span class="sxs-lookup"><span data-stu-id="772f9-p102">Specifying MS Remote as the provider for the <STRONG>RDS.DataControl</STRONG> would create a four-tier scenario. Scenarios greater than three tiers have not been tested and should not be needed.</span></span></P>



  - <span data-ttu-id="772f9-115">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="772f9-115">*DataControl*</span></span>

  - <span data-ttu-id="772f9-116">**RDS.DataControl** オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="772f9-116">An object variable that represents an **RDS.DataControl** object.</span></span>

