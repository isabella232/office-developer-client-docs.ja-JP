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
ms.openlocfilehash: 31f5e0b4dbb924c57c6a94e80cfb98e119292bd7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922490"
---
# <a name="recordset2parentrecordset-property-dao"></a><span data-ttu-id="58e33-102">Recordset2.ParentRecordset プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="58e33-102">Recordset2.ParentRecordset property (DAO)</span></span>


<span data-ttu-id="58e33-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="58e33-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="58e33-p101">指定したレコードセットの親 **Recordset** を返します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="58e33-p101">Returns the parent **Recordset** of the specified recordset. Read-only.</span></span>

## <a name="version-information"></a><span data-ttu-id="58e33-106">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="58e33-106">Version Information</span></span>

<span data-ttu-id="58e33-107">追加バージョン: Access 2007</span><span class="sxs-lookup"><span data-stu-id="58e33-107">Version Added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="58e33-108">構文</span><span class="sxs-lookup"><span data-stu-id="58e33-108">Syntax</span></span>

<span data-ttu-id="58e33-109">*式*です。ParentRecordset</span><span class="sxs-lookup"><span data-stu-id="58e33-109">*expression* .ParentRecordset</span></span>

<span data-ttu-id="58e33-110">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="58e33-110">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="58e33-111">注釈</span><span class="sxs-lookup"><span data-stu-id="58e33-111">Remarks</span></span>

<span data-ttu-id="58e33-112">指定されたレコードセットが複数値を持つフィールドを表していない場合、 **ParentRecordset** プロパティは **Null** を返します。</span><span class="sxs-lookup"><span data-stu-id="58e33-112">The **ParentRecordset** property returns **Null** if the specifed recordset does not represent a multi-valued field.</span></span>

