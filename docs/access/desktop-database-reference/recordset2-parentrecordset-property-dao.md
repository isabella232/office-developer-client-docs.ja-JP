---
title: Recordset2.ParentRecordset プロパティ (DAO)
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
ms.openlocfilehash: 8c20baea6600ce3b2c86c638ce87df864c1acfaa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479062"
---
# <a name="recordset2parentrecordset-property-dao"></a><span data-ttu-id="c6604-102">Recordset2.ParentRecordset プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="c6604-102">Recordset2.ParentRecordset Property (DAO)</span></span>


<span data-ttu-id="c6604-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6604-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="c6604-p101">指定したレコードセットの親 **Recordset** を返します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="c6604-p101">Returns the parent **Recordset** of the specified recordset. Read-only.</span></span>

## <a name="version-information"></a><span data-ttu-id="c6604-106">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="c6604-106">Version Information</span></span>

<span data-ttu-id="c6604-107">追加バージョン: Access 2007</span><span class="sxs-lookup"><span data-stu-id="c6604-107">Version Added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="c6604-108">構文</span><span class="sxs-lookup"><span data-stu-id="c6604-108">Syntax</span></span>

<span data-ttu-id="c6604-109">*式*です。ParentRecordset</span><span class="sxs-lookup"><span data-stu-id="c6604-109">*expression* .ParentRecordset</span></span>

<span data-ttu-id="c6604-110">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="c6604-110">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6604-111">注釈</span><span class="sxs-lookup"><span data-stu-id="c6604-111">Remarks</span></span>

<span data-ttu-id="c6604-112">指定されたレコードセットが複数値を持つフィールドを表していない場合、 **ParentRecordset** プロパティは **Null** を返します。</span><span class="sxs-lookup"><span data-stu-id="c6604-112">The **ParentRecordset** property returns **Null** if the specifed recordset does not represent a multi-valued field.</span></span>

