---
title: QueryDef.LastUpdated プロパティ (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 3b7818d4-054e-54e2-bf63-58b340bb4a90
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192665(v=office.15)
ms:contentKeyID: 48544287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98bb600e6f3f1c9587eca110269e8b6b3765e40f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921273"
---
# <a name="querydeflastupdated-property-dao"></a><span data-ttu-id="17183-102">QueryDef.LastUpdated プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="17183-102">QueryDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="17183-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="17183-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17183-p101">オブジェクトに対して行われた最新の変更の日付と時刻を取得します。値の取得のみ可能です。バリアント型 ( **Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="17183-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="17183-106">構文</span><span class="sxs-lookup"><span data-stu-id="17183-106">Syntax</span></span>

<span data-ttu-id="17183-107">*式*です。LastUpdated</span><span class="sxs-lookup"><span data-stu-id="17183-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="17183-108">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="17183-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="17183-109">注釈</span><span class="sxs-lookup"><span data-stu-id="17183-109">Remarks</span></span>

<span data-ttu-id="17183-p102">**DateCreated** プロパティおよび **LastUpdated** プロパティは、オブジェクトが作成された日付および時刻、または最後に更新された日付および時刻を取得します。マルチユーザー環境では、ユーザーがファイル サーバーから直接これらの設定を取得し、DateCreated プロパティおよび LastUpdated プロパティの設定値が一致しなくなるのを防ぐ必要があります。</span><span class="sxs-lookup"><span data-stu-id="17183-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

