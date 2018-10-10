---
title: TableDef.Updatable プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44f24e68b60f69304a167d2b9b5ce0b4b0e69b11
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479544"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="6d259-102">TableDef.Updatable プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="6d259-102">TableDef.Updatable Property (DAO)</span></span>


<span data-ttu-id="6d259-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d259-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6d259-p101">DAO オブジェクトを変更できるかどうかを示す値を取得します。値の取得のみ可能です。ブール型 ( **Boolean**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6d259-p101">Returns a value that indicates whether you can change a DAO object. Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d259-106">構文</span><span class="sxs-lookup"><span data-stu-id="6d259-106">Syntax</span></span>

<span data-ttu-id="6d259-107">*式*です。更新可能です</span><span class="sxs-lookup"><span data-stu-id="6d259-107">*expression* .Updatable</span></span>

<span data-ttu-id="6d259-108">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="6d259-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d259-109">注釈</span><span class="sxs-lookup"><span data-stu-id="6d259-109">Remarks</span></span>

<span data-ttu-id="6d259-p102">**Updatable** プロパティの設定値は常に、新しく作成した **TableDef** オブジェクトでは **True**、リンクされた **TableDef** オブジェクトでは **False** となります。新しい **TableDef** オブジェクトは、現在のユーザーが書き込み権限を持つデータベースにのみ追加できます。</span><span class="sxs-lookup"><span data-stu-id="6d259-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>
