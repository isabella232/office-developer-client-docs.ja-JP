---
title: Recordset2 recordset プロパティ (DAO)
TOCTitle: ParentRecordset Property
ms:assetid: 816cc92e-e530-6ca6-65b0-3165221835a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196492(v=office.15)
ms:contentKeyID: 48545948
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101188
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7424e31e7f351af02bdd54bd06fe41f7db5b5f54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309075"
---
# <a name="recordset2parentrecordset-property-dao"></a><span data-ttu-id="1a5d1-102">Recordset2 recordset プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="1a5d1-102">Recordset2.ParentRecordset property (DAO)</span></span>


<span data-ttu-id="1a5d1-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a5d1-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="1a5d1-104">指定したレコードセットの親 **Recordset** を返します。</span><span class="sxs-lookup"><span data-stu-id="1a5d1-104">Returns the parent **Recordset** of the specified recordset.</span></span> <span data-ttu-id="1a5d1-105">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="1a5d1-105">Read-only.</span></span>

## <a name="version-information"></a><span data-ttu-id="1a5d1-106">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="1a5d1-106">Version information</span></span>

<span data-ttu-id="1a5d1-107">追加されたバージョン: Access 2007</span><span class="sxs-lookup"><span data-stu-id="1a5d1-107">Version added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="1a5d1-108">構文</span><span class="sxs-lookup"><span data-stu-id="1a5d1-108">Syntax</span></span>

<span data-ttu-id="1a5d1-109">*式*。ParentRecordset</span><span class="sxs-lookup"><span data-stu-id="1a5d1-109">*expression* .ParentRecordset</span></span>

<span data-ttu-id="1a5d1-110">\*式\***Recordset2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="1a5d1-110">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a5d1-111">注釈</span><span class="sxs-lookup"><span data-stu-id="1a5d1-111">Remarks</span></span>

<span data-ttu-id="1a5d1-112">指定されたレコードセットが複数値を持つフィールドを表していない場合、 **ParentRecordset** プロパティは **Null** を返します。</span><span class="sxs-lookup"><span data-stu-id="1a5d1-112">The **ParentRecordset** property returns **Null** if the specifed recordset does not represent a multi-valued field.</span></span>

