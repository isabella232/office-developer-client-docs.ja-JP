---
title: ADORecordConstruction インターフェイス (ADO)
TOCTitle: ADORecordConstruction interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a53eb107bab0d31606dc161b9f9c910894c5bc6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281627"
---
# <a name="adorecordconstruction-interface-ado"></a><span data-ttu-id="4a40e-102">ADORecordConstruction インターフェイス (ADO)</span><span class="sxs-lookup"><span data-stu-id="4a40e-102">ADORecordConstruction interface (ADO)</span></span>


<span data-ttu-id="4a40e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="4a40e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4a40e-104">**ADORecordConstruction** インターフェイスは、C/C++ アプリケーションで OLE DB **Row** から ADO **Record** オブジェクトを作成するために使用します。</span><span class="sxs-lookup"><span data-stu-id="4a40e-104">The **ADORecordConstruction** interface is used to construct an ADO **Record** object from an OLE DB **Row** object in a C/C++ application.</span></span>

<span data-ttu-id="4a40e-105">このインターフェイスでは、以下のプロパティがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="4a40e-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="4a40e-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="4a40e-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4a40e-107"><a href="parentrow-property-ado.md">ParentRow</a></span><span class="sxs-lookup"><span data-stu-id="4a40e-107"><a href="parentrow-property-ado.md">ParentRow</a></span></span></p></td>
<td><p><span data-ttu-id="4a40e-108">書き込み専用です。</span><span class="sxs-lookup"><span data-stu-id="4a40e-108">Write-only.</span></span><br />
<span data-ttu-id="4a40e-109">
ADO <strong>Record</strong> オブジェクトに対する OLE DB <strong>Row</strong> オブジェクトのコンテナーを設定します。</span><span class="sxs-lookup"><span data-stu-id="4a40e-109">Sets the container of an OLE DB <strong>Row</strong> object on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4a40e-110"><a href="row-property-ado.md">行</a></span><span class="sxs-lookup"><span data-stu-id="4a40e-110"><a href="row-property-ado.md">Row</a></span></span></p></td>
<td><p><span data-ttu-id="4a40e-111">読み取り/書き込み可能。</span><span class="sxs-lookup"><span data-stu-id="4a40e-111">Read/Write.</span></span><br />
<span data-ttu-id="4a40e-112">
ADO <strong>Record</strong> オブジェクトに対する OLE DB <strong>Row</strong> オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4a40e-112">Gets/sets an OLE DB <strong>Row</strong> object from/on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="4a40e-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="4a40e-113">Methods</span></span>

<span data-ttu-id="4a40e-114">なし。</span><span class="sxs-lookup"><span data-stu-id="4a40e-114">None.</span></span>

## <a name="events"></a><span data-ttu-id="4a40e-115">イベント</span><span class="sxs-lookup"><span data-stu-id="4a40e-115">Events</span></span>

<span data-ttu-id="4a40e-116">なし。</span><span class="sxs-lookup"><span data-stu-id="4a40e-116">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a40e-117">注釈</span><span class="sxs-lookup"><span data-stu-id="4a40e-117">Remarks</span></span>

<span data-ttu-id="4a40e-118">OLE DB **Row**オブジェクト (prow)、ado record オブジェクト (adoR) の\*\*\*\* 構造、および次の3つの基本的な\*\*\*\* 操作に対する金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="4a40e-118">Given an OLE DB **Row** object (pRow), the construction of an ADO **Record** object (), the construction of an ADO **Record** object (adoR), amounts to the following three basic operations:</span></span>

1.  <span data-ttu-id="4a40e-119">ADO **Record** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="4a40e-119">Create an ADO **Record** object:</span></span>
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  <span data-ttu-id="4a40e-120">**IADORecordConstruction** インターフェイスで **Record** オブジェクトを照会します。</span><span class="sxs-lookup"><span data-stu-id="4a40e-120">Query the **IADORecordConstruction** interface on the **Record** object:</span></span>
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  <span data-ttu-id="4a40e-121">**IADORecordConstruction::p ut\_row**プロパティメソッドを呼び出して、ADO **Record**オブジェクトの OLE DB **Row**オブジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="4a40e-121">Call the **IADORecordConstruction::put\_Row** property method to set the OLE DB **Row** object on the ADO **Record** object:</span></span>
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
<span data-ttu-id="4a40e-122">結果として得られた **adoR** オブジェクトは、OLE DB **Row** から作成された ADO **Record** オブジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="4a40e-122">The resultant **adoR** object now represents the ADO **Record** object constructed from the OLE DB **Row** object.</span></span>

<span data-ttu-id="4a40e-123">ADO **Record** オブジェクトは、OLE DB **Row** オブジェクトのコンテナーからも作成できます。</span><span class="sxs-lookup"><span data-stu-id="4a40e-123">An ADO **Record** object can also be constructed from the container of an OLE DB **Row** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a40e-124">要件</span><span class="sxs-lookup"><span data-stu-id="4a40e-124">Requirements</span></span>

<span data-ttu-id="4a40e-125">**バージョン:** ADO 2.0 以上</span><span class="sxs-lookup"><span data-stu-id="4a40e-125">**Version:** ADO 2.0 and later</span></span>

<span data-ttu-id="4a40e-126">**ライブラリ:** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="4a40e-126">**Library:** msado15.dll</span></span>

<span data-ttu-id="4a40e-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="4a40e-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span></span>

