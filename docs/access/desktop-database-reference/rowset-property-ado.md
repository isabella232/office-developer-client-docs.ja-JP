---
title: Rowset プロパティ (ADO)
TOCTitle: Rowset Property (ADO)
ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15)
ms:contentKeyID: 48543515
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 95a33fb3d24e5cdbf608d268781be0dd536fa315
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477920"
---
# <a name="rowset-property-ado"></a><span data-ttu-id="98b7c-102">Rowset プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="98b7c-102">Rowset Property (ADO)</span></span>


<span data-ttu-id="98b7c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="98b7c-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="98b7c-104">**ADORecordsetConstruction** オブジェクトの OLE DB **Rowset** オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="98b7c-104">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="98b7c-105">Put を使用すると、\_、ADO**レコード セット**オブジェクトに、行セットの行セットが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="98b7c-105">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="98b7c-106">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="98b7c-106">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b7c-107">構文</span><span class="sxs-lookup"><span data-stu-id="98b7c-107">Syntax</span></span>

<span data-ttu-id="98b7c-108">HRESULT get\_行セット (\[、戻り値を\]IUnknown\* \* ppRowset)。</span><span class="sxs-lookup"><span data-stu-id="98b7c-108">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="98b7c-109">HRESULT に\_の行セット (\[の\]IUnknown\*ため)。</span><span class="sxs-lookup"><span data-stu-id="98b7c-109">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="98b7c-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="98b7c-110">Parameters</span></span>

  - <span data-ttu-id="98b7c-111">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="98b7c-111">*ppRowset*</span></span>

  - <span data-ttu-id="98b7c-112">OLE DB **Rowset** オブジェクトを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="98b7c-112">Pointer to an OLE DB **Rowset** object.</span></span>

  - <span data-ttu-id="98b7c-113">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="98b7c-113">*PRowset*</span></span>

  - <span data-ttu-id="98b7c-114">OLE DB **Rowset** オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="98b7c-114">An OLE DB **Rowset** object.</span></span>

## <a name="return-values"></a><span data-ttu-id="98b7c-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="98b7c-115">Return Values</span></span>

<span data-ttu-id="98b7c-116">このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。</span><span class="sxs-lookup"><span data-stu-id="98b7c-116">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="98b7c-117">対象</span><span class="sxs-lookup"><span data-stu-id="98b7c-117">Applies To</span></span>

[<span data-ttu-id="98b7c-118">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="98b7c-118">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

