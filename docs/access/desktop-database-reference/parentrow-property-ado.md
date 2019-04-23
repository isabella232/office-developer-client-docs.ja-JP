---
title: parentrow プロパティ (ADO)
TOCTitle: ParentRow property (ADO)
ms:assetid: c7520353-9428-9c8f-9d21-ff42e30e1193
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249971(v=office.15)
ms:contentKeyID: 48547638
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2844f7c93164c4b384a895cd32a13bd682154ce3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287739"
---
# <a name="parentrow-property-ado"></a><span data-ttu-id="b1251-102">parentrow プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="b1251-102">ParentRow property (ADO)</span></span>

<span data-ttu-id="b1251-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b1251-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b1251-104">OLE DB **Row** オブジェクトのコンテナーを **ADORecordConstruction** オブジェクトに設定し、行の親が ADO **Record** オブジェクトに変換されるようにします。</span><span class="sxs-lookup"><span data-stu-id="b1251-104">Sets the container of an OLE DB **Row** object on an **ADORecordConstruction** object, so that the parent of the row is turned into an ADO **Record** object.</span></span>

<span data-ttu-id="b1251-105">値の設定のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="b1251-105">Write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1251-106">構文</span><span class="sxs-lookup"><span data-stu-id="b1251-106">Syntax</span></span>

<span data-ttu-id="b1251-107">HRESULT put\_parentrow (\[\] IUnknown\* pparent)。</span><span class="sxs-lookup"><span data-stu-id="b1251-107">HRESULT put\_ParentRow(\[in\] IUnknown\* pParent);</span></span>

## <a name="parameters"></a><span data-ttu-id="b1251-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1251-108">Parameters</span></span>

|<span data-ttu-id="b1251-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b1251-109">Parameter</span></span>|<span data-ttu-id="b1251-110">説明</span><span class="sxs-lookup"><span data-stu-id="b1251-110">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b1251-111">*pparent*</span><span class="sxs-lookup"><span data-stu-id="b1251-111">*pParent*</span></span> |<span data-ttu-id="b1251-112">行のコンテナー。</span><span class="sxs-lookup"><span data-stu-id="b1251-112">A container of a row.</span></span>|

## <a name="return-values"></a><span data-ttu-id="b1251-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="b1251-113">Return values</span></span>

<span data-ttu-id="b1251-114">このプロパティメソッドは、S\_OK および E\_FAIL を含む標準の HRESULT 値を返します。</span><span class="sxs-lookup"><span data-stu-id="b1251-114">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="b1251-115">適用対象</span><span class="sxs-lookup"><span data-stu-id="b1251-115">Applies to</span></span>

[<span data-ttu-id="b1251-116">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="b1251-116">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

