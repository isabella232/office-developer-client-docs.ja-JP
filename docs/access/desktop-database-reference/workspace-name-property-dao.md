---
title: Workspace.Name プロパティ (DAO)
TOCTitle: Name Property
ms:assetid: 6bfdf1e3-b396-ba30-0453-92624a433624
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195490(v=office.15)
ms:contentKeyID: 48545464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cda13f1a377a7e730839df854124d05a4d93ea92
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881161"
---
# <a name="workspacename-property-dao"></a><span data-ttu-id="72371-102">Workspace.Name プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="72371-102">Workspace.Name Property (DAO)</span></span>


<span data-ttu-id="72371-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="72371-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="72371-p101">指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="72371-p101">Returns or sets the name of the specified object. Read/write **String** if the object has not been appended to a collection. Read-only **String** if the object has been appended to a collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="72371-107">構文</span><span class="sxs-lookup"><span data-stu-id="72371-107">Syntax</span></span>

<span data-ttu-id="72371-108">*式*です。名</span><span class="sxs-lookup"><span data-stu-id="72371-108">*expression* .Name</span></span>

<span data-ttu-id="72371-109">\*式\***ワークスペース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="72371-109">*expression* A variable that represents a **Workspace** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="72371-110">注釈</span><span class="sxs-lookup"><span data-stu-id="72371-110">Remarks</span></span>

<span data-ttu-id="72371-111">**Workspace** オブジェクト名の最大長は 20 文字です。</span><span class="sxs-lookup"><span data-stu-id="72371-111">The maximum length for the name of a **Workspace** object is 20 characters.</span></span>

