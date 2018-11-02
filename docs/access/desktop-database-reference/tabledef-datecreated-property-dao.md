---
title: TableDef.DateCreated プロパティ (DAO)
TOCTitle: DateCreated Property
ms:assetid: fedd28e9-41a4-db7f-9ba9-6ada350d594a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837292(v=office.15)
ms:contentKeyID: 48548947
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: be76ed7f9d358963ea58776327ddafbb66f9d367
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923141"
---
# <a name="tabledefdatecreated-property-dao"></a><span data-ttu-id="cecc3-102">TableDef.DateCreated プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="cecc3-102">TableDef.DateCreated property (DAO)</span></span>


<span data-ttu-id="cecc3-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cecc3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cecc3-p101">オブジェクトを作成した日付と時刻を取得します (Microsoft Access ワークスペースのみ)。値の取得のみ可能です。バリアント型 ( **Variant**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cecc3-p101">Returns the date and time that an object was created (Microsoft Access workspaces only). Read-only **Variant**.</span></span>

## <a name="syntax"></a><span data-ttu-id="cecc3-106">構文</span><span class="sxs-lookup"><span data-stu-id="cecc3-106">Syntax</span></span>

<span data-ttu-id="cecc3-107">*式*です。作成日時</span><span class="sxs-lookup"><span data-stu-id="cecc3-107">*expression* .DateCreated</span></span>

<span data-ttu-id="cecc3-108">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="cecc3-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="cecc3-109">注釈</span><span class="sxs-lookup"><span data-stu-id="cecc3-109">Remarks</span></span>

<span data-ttu-id="cecc3-p102">**DateCreated** プロパティおよび **LastUpdated** プロパティは、オブジェクトが作成された日付および時刻、または最後に更新された日付および時刻を取得します。マルチユーザー環境では、ユーザーがファイル サーバーから直接これらの設定を取得し、DateCreated プロパティおよび LastUpdated プロパティの設定値が一致しなくなるのを防ぐ必要があります。</span><span class="sxs-lookup"><span data-stu-id="cecc3-p102">**DateCreated** and **LastUpdated** return the date and time that the object was created or last updated. In a multiuser environment, users should get these settings directly from the file server to avoid discrepancies in the DateCreated and LastUpdated property settings.</span></span>

