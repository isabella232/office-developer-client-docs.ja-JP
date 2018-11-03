---
title: TableDef.LastUpdated プロパティ (DAO)
TOCTitle: LastUpdated Property
ms:assetid: fafe54e2-2cf0-5874-92b9-6e20a65e77ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837164(v=office.15)
ms:contentKeyID: 48548859
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 81d8dfd040ef7df954b71f724ed1d2689d5d4b33
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928223"
---
# <a name="tabledeflastupdated-property-dao"></a><span data-ttu-id="f6be8-102">TableDef.LastUpdated プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="f6be8-102">TableDef.LastUpdated property (DAO)</span></span>


<span data-ttu-id="f6be8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f6be8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6be8-p101">オブジェクトに対して行われた最新の変更の日付と時刻を取得します。値の取得のみ可能です。バリアント型 ( **Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f6be8-p101">Returns the date and time of the most recent change made to an object. Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6be8-106">構文</span><span class="sxs-lookup"><span data-stu-id="f6be8-106">Syntax</span></span>

<span data-ttu-id="f6be8-107">*式*です。LastUpdated</span><span class="sxs-lookup"><span data-stu-id="f6be8-107">*expression* .LastUpdated</span></span>

<span data-ttu-id="f6be8-108">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="f6be8-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6be8-109">注釈</span><span class="sxs-lookup"><span data-stu-id="f6be8-109">Remarks</span></span>

<span data-ttu-id="f6be8-p102">**DateCreated** プロパティおよび **LastUpdated** プロパティは、オブジェクトが作成された日付および時刻、または最後に更新された日付および時刻を取得します。マルチユーザー環境では、ユーザーがファイル サーバーから直接これらの設定を取得し、DateCreated プロパティおよび LastUpdated プロパティの設定値が一致しなくなるのを防ぐ必要があります。</span><span class="sxs-lookup"><span data-stu-id="f6be8-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

