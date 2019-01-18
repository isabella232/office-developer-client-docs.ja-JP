---
title: ParentRow プロパティ (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2844f7c93164c4b384a895cd32a13bd682154ce3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721725"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="83237-102">ParentRow プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="83237-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="83237-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="83237-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="83237-104">OLE DB **Row** オブジェクトのコンテナーを **ADORecordConstruction** オブジェクトに設定し、行の親が ADO **Record** オブジェクトに変換されるようにします。</span><span class="sxs-lookup"><span data-stu-id="83237-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="83237-105">値の設定のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="83237-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="83237-106">構文</span><span class="sxs-lookup"><span data-stu-id="83237-106">Syntax</span></span>

<span data-ttu-id="83237-107">HRESULT に\_ParentRow (\[の\]IUnknown\* pParent)。</span><span class="sxs-lookup"><span data-stu-id="83237-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="83237-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83237-108">Parameters</span></span>

|<span data-ttu-id="83237-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="83237-109">Parameter</span></span>|<span data-ttu-id="83237-110">説明</span><span class="sxs-lookup"><span data-stu-id="83237-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="83237-111">*pParent*</span><span class="sxs-lookup"><span data-stu-id="83237-111">*pParent*</span></span> |<span data-ttu-id="83237-112">行のコンテナー。</span><span class="sxs-lookup"><span data-stu-id="83237-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="83237-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="83237-113">Return values</span></span>

<span data-ttu-id="83237-114">このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。</span><span class="sxs-lookup"><span data-stu-id="83237-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="83237-115">適用対象</span><span class="sxs-lookup"><span data-stu-id="83237-115">Applies to</span></span>

[<span data-ttu-id="83237-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="83237-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

