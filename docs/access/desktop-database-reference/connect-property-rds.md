---
title: Connect プロパティ (RDS)
TOCTitle: Connect property (RDS)
ms:assetid: 11aa3284-18e9-6d2d-761b-c25090370b77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248890(v=office.15)
ms:contentKeyID: 48543324
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ebd9eb25e2e0e6b9b2233ff0d9faf8c3e369f0f9
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925262"
---
# <a name="connect-property-rds"></a><span data-ttu-id="6b3dd-102">Connect プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="6b3dd-102">Connect property (RDS)</span></span>


<span data-ttu-id="6b3dd-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6b3dd-104">クエリおよび更新操作が実行されるデータベース名を示します。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-104">Indicates the database name from which the query and update operations are run.</span></span>

<span data-ttu-id="6b3dd-105">**Connect** プロパティは、デザイン時に [RDS.DataControl](datacontrol-object-rds.md) オブジェクトの OBJECT タグ内で、または実行時にスクリプト コード (たとえば、VBScript) 内で設定できます。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-105">You can set the **Connect** property at design time in the [RDS.DataControl](datacontrol-object-rds.md) object's OBJECT tags, or at run time in scripting code (for instance, VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="6b3dd-106">構文</span><span class="sxs-lookup"><span data-stu-id="6b3dd-106">Syntax</span></span>

<span data-ttu-id="6b3dd-107">デザイン時:\<パラメーターの名前 [接続] の値を = =「接続文字列」\></span><span class="sxs-lookup"><span data-stu-id="6b3dd-107">Design time: \<PARAM NAME="Connect" VALUE="ConnectionString"\></span></span>

<span data-ttu-id="6b3dd-108">実行時間: DataControl.Connect =「接続文字列」</span><span class="sxs-lookup"><span data-stu-id="6b3dd-108">Run time: DataControl.Connect = "ConnectionString"</span></span>

## <a name="parameters"></a><span data-ttu-id="6b3dd-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6b3dd-109">Parameters</span></span>

- <span data-ttu-id="6b3dd-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="6b3dd-110">*ConnectionString*</span></span>

  - <span data-ttu-id="6b3dd-p101">有効な接続文字列を指定します。接続文字列全般の説明については、[ConnectionString](connectionstring-property-ado.md) プロパティかプロバイダーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-p101">A valid connection string. For more general information about connection strings, see the [ConnectionString](connectionstring-property-ado.md) property or your provider documentation.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="6b3dd-p102">[!メモ] **RDS.DataControl** のプロバイダーとして MS Remote を指定すると、4 層のシナリオが作成されます。3 層を超えるシナリオについては未確認なので避けてください。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-p102">Specifying MS Remote as the provider for the **RDS.DataControl** would create a four-tier scenario. Scenarios greater than three tiers have not been tested and should not be needed.</span></span>

- <span data-ttu-id="6b3dd-115">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="6b3dd-115">*DataControl*</span></span>

  - <span data-ttu-id="6b3dd-116">**RDS.DataControl** オブジェクトを表すオブジェクト変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6b3dd-116">An object variable that represents an **RDS.DataControl** object.</span></span>

