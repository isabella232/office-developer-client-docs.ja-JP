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
ms.openlocfilehash: 8b418b63e0c89246ac2caa88c98ea1d4e490cbbb
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937646"
---
# <a name="recordset2parentrecordset-property-dao"></a><span data-ttu-id="ec8b8-102">Recordset2.ParentRecordset プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="ec8b8-102">Recordset2.ParentRecordset property (DAO)</span></span>


<span data-ttu-id="ec8b8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ec8b8-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="ec8b8-p101">指定したレコードセットの親 **Recordset** を返します。値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="ec8b8-p101">Returns the parent **Recordset** of the specified recordset. Read-only.</span></span>

## <a name="version-information"></a><span data-ttu-id="ec8b8-106">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="ec8b8-106">Version information</span></span>

<span data-ttu-id="ec8b8-107">追加バージョン: Access 2007</span><span class="sxs-lookup"><span data-stu-id="ec8b8-107">Version added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="ec8b8-108">構文</span><span class="sxs-lookup"><span data-stu-id="ec8b8-108">Syntax</span></span>

<span data-ttu-id="ec8b8-109">*式*です。ParentRecordset</span><span class="sxs-lookup"><span data-stu-id="ec8b8-109">*expression* .ParentRecordset</span></span>

<span data-ttu-id="ec8b8-110">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="ec8b8-110">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec8b8-111">注釈</span><span class="sxs-lookup"><span data-stu-id="ec8b8-111">Remarks</span></span>

<span data-ttu-id="ec8b8-112">指定されたレコードセットが複数値を持つフィールドを表していない場合、 **ParentRecordset** プロパティは **Null** を返します。</span><span class="sxs-lookup"><span data-stu-id="ec8b8-112">The **ParentRecordset** property returns **Null** if the specifed recordset does not represent a multi-valued field.</span></span>

