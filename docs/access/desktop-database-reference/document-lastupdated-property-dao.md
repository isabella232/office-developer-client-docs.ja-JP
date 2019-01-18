---
title: Document.LastUpdated プロパティ (DAO)
TOCTitle: LastUpdated Property
ms:assetid: 9307ceee-095f-0364-fd5b-905bc523b9c0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197661(v=office.15)
ms:contentKeyID: 48546388
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: abb766f7a47cbacaededf65eb2b5e9145bf88c60
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698380"
---
# <a name="documentlastupdated-property-dao"></a><span data-ttu-id="d96ce-102">Document.LastUpdated プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="d96ce-102">Document.LastUpdated property (DAO)</span></span>


<span data-ttu-id="d96ce-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d96ce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d96ce-p101">オブジェクトに対して行われた最新の変更の日付と時刻を取得します。値の取得のみ可能です。バリアント型 ( **Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d96ce-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d96ce-106">構文</span><span class="sxs-lookup"><span data-stu-id="d96ce-106">Syntax</span></span>

<span data-ttu-id="d96ce-107">*式*です。LastUpdated</span><span class="sxs-lookup"><span data-stu-id="d96ce-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="d96ce-108">\*式\***ドキュメント**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="d96ce-108">*expression* A variable that represents a **Document** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d96ce-109">注釈</span><span class="sxs-lookup"><span data-stu-id="d96ce-109">Remarks</span></span>

<span data-ttu-id="d96ce-p102">**DateCreated** プロパティおよび **LastUpdated** プロパティは、オブジェクトが作成された日付および時刻、または最後に更新された日付および時刻を取得します。マルチユーザー環境では、ユーザーがファイル サーバーから直接これらの設定を取得し、DateCreated プロパティおよび LastUpdated プロパティの設定値が一致しなくなるのを防ぐ必要があります。</span><span class="sxs-lookup"><span data-stu-id="d96ce-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

