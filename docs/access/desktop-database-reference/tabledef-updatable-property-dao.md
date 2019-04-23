---
title: TableDef プロパティ (DAO)
TOCTitle: Updatable Property
ms:assetid: 0b1ae7e5-416d-06f0-5d74-989c6db67ff2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845128(v=office.15)
ms:contentKeyID: 48543168
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6e6c7409b89058c6be55d9fb83eb85c7af9fb9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314414"
---
# <a name="tabledefupdatable-property-dao"></a><span data-ttu-id="f1ea1-102">TableDef プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="f1ea1-102">TableDef.Updatable property (DAO)</span></span>


<span data-ttu-id="f1ea1-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="f1ea1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f1ea1-104">DAO オブジェクトを変更できるかどうかを示す値を返します。</span><span class="sxs-lookup"><span data-stu-id="f1ea1-104">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="f1ea1-105">値の取得のみ可能なブール型 (**Boolean**) の値です。</span><span class="sxs-lookup"><span data-stu-id="f1ea1-105">Read-only **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ea1-106">構文</span><span class="sxs-lookup"><span data-stu-id="f1ea1-106">Syntax</span></span>

<span data-ttu-id="f1ea1-107">*式*。できる</span><span class="sxs-lookup"><span data-stu-id="f1ea1-107">*expression* .Updatable</span></span>

<span data-ttu-id="f1ea1-108">\*式\***TableDef**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="f1ea1-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1ea1-109">注釈</span><span class="sxs-lookup"><span data-stu-id="f1ea1-109">Remarks</span></span>

<span data-ttu-id="f1ea1-p102">**Updatable** プロパティの設定値は常に、新しく作成した **TableDef** オブジェクトでは **True**、リンクされた **TableDef** オブジェクトでは **False** となります。新しい **TableDef** オブジェクトは、現在のユーザーが書き込み権限を持つデータベースにのみ追加できます。</span><span class="sxs-lookup"><span data-stu-id="f1ea1-p102">The **Updatable** property setting is always **True** for a newly created **TableDef** object and **False** for a linked **TableDef** object. A new **TableDef** object can be appended only to a database for which the current user has write permission.</span></span>

