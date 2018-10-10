---
title: Document.LastUpdated プロパティ (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f8192dc32554b29c9fe024f34f08757cb512aa5b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479459"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="2f812-102">Document.LastUpdated プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="2f812-102">Document.LastUpdated Property (DAO)</span></span>


<span data-ttu-id="2f812-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f812-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2f812-p101">オブジェクトに対して行われた最新の変更の日付と時刻を取得します。値の取得のみ可能です。バリアント型 ( **Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2f812-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f812-106">構文</span><span class="sxs-lookup"><span data-stu-id="2f812-106">Syntax</span></span>

<span data-ttu-id="2f812-107">*式*です。LastUpdated</span><span class="sxs-lookup"><span data-stu-id="2f812-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="2f812-108">\*式\***ドキュメント**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="2f812-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f812-109">注釈</span><span class="sxs-lookup"><span data-stu-id="2f812-109">Remarks</span></span>

<span data-ttu-id="2f812-p102">**DateCreated** プロパティおよび **LastUpdated** プロパティは、オブジェクトが作成された日付および時刻、または最後に更新された日付および時刻を取得します。マルチユーザー環境では、ユーザーがファイル サーバーから直接これらの設定を取得し、DateCreated プロパティおよび LastUpdated プロパティの設定値が一致しなくなるのを防ぐ必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f812-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

