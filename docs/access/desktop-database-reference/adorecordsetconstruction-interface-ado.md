---
title: ADORecordsetConstruction インターフェイス (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 98342d5456c545e6da8539c11f616c08fd52a932
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281634"
---
# <a name="adorecordsetconstruction-interface-ado"></a><span data-ttu-id="37b71-102">ADORecordsetConstruction インターフェイス (ADO)</span><span class="sxs-lookup"><span data-stu-id="37b71-102">ADORecordsetConstruction interface (ADO)</span></span>


<span data-ttu-id="37b71-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="37b71-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="37b71-104">. **ADORecordsetConstruction** インターフェイスは、C/C++ アプリケーションで OLE DB **Rowset** オブジェクトから ADO **Recordset** オブジェクトを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="37b71-104">The **ADORecordsetConstruction** interface is used to construct an ADO **Recordset** object from an OLE DB **Rowset** object in a C/C++ application.</span></span>

<span data-ttu-id="37b71-105">このインターフェイスでは、以下のプロパティがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="37b71-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="37b71-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="37b71-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37b71-107"><a href="chapter-property-ado.md">節</a></span><span class="sxs-lookup"><span data-stu-id="37b71-107"><a href="chapter-property-ado.md">Chapter</a></span></span></p></td>
<td><p><span data-ttu-id="37b71-108">読み取り/書き込み可能。</span><span class="sxs-lookup"><span data-stu-id="37b71-108">Read/Write.</span></span><br />
<span data-ttu-id="37b71-109">
ADO <strong>Recordset</strong> オブジェクトに対する OLE DB <strong>Chapter</strong> オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37b71-109">Gets/sets an OLE DB <strong>Chapter</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37b71-110"><a href="rowposition-property-ado.md">RowPosition</a></span><span class="sxs-lookup"><span data-stu-id="37b71-110"><a href="rowposition-property-ado.md">RowPosition</a></span></span></p></td>
<td><p><span data-ttu-id="37b71-111">読み取り/書き込み可能。</span><span class="sxs-lookup"><span data-stu-id="37b71-111">Read/Write.</span></span><br />
<span data-ttu-id="37b71-112">
ADO <strong>Recordset</strong> オブジェクトに対する OLE DB <strong>RowPosition</strong> オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37b71-112">Gets/sets an OLE DB <strong>RowPosition</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37b71-113"><a href="rowset-property-ado.md">行</a></span><span class="sxs-lookup"><span data-stu-id="37b71-113"><a href="rowset-property-ado.md">Rowset</a></span></span></p></td>
<td><p><span data-ttu-id="37b71-114">読み取り/書き込み可能。</span><span class="sxs-lookup"><span data-stu-id="37b71-114">Read/Write.</span></span><br />
<span data-ttu-id="37b71-115">
ADO <strong>Recordset</strong> オブジェクトに対する OLE DB <strong>Rowset</strong> オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="37b71-115">Gets/sets an OLE DB <strong>Rowset</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="37b71-116">メソッド</span><span class="sxs-lookup"><span data-stu-id="37b71-116">Methods</span></span>

<span data-ttu-id="37b71-117">なし。</span><span class="sxs-lookup"><span data-stu-id="37b71-117">None.</span></span>

## <a name="events"></a><span data-ttu-id="37b71-118">イベント</span><span class="sxs-lookup"><span data-stu-id="37b71-118">Events</span></span>

<span data-ttu-id="37b71-119">なし。</span><span class="sxs-lookup"><span data-stu-id="37b71-119">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="37b71-120">注釈</span><span class="sxs-lookup"><span data-stu-id="37b71-120">Remarks</span></span>

<span data-ttu-id="37b71-121">OLE DB **Rowset**オブジェクト (pRowset) (ado **recordset**オブジェクトの構造) () を指定すると、ado **recordset**オブジェクト (adors) の構造は次の3つの基本的な操作になります。</span><span class="sxs-lookup"><span data-stu-id="37b71-121">Given an OLE DB **Rowset** object (pRowset ), the construction of an ADO **Recordset** object (), the construction of an ADO **Recordset** object (adoRs ) amounts to the following three basic operations:</span></span>

1. <span data-ttu-id="37b71-122">ADO **Recordset** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="37b71-122">Create an ADO **Recordset** object:</span></span>
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. <span data-ttu-id="37b71-123">**IADORecordsetConstruction** インターフェイスで **Recordset** オブジェクトを照会します。</span><span class="sxs-lookup"><span data-stu-id="37b71-123">Query the **IADORecordsetConstruction** interface on the **Recordset** object:</span></span>

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. <span data-ttu-id="37b71-124">IADORecordsetConstruction::p ut\_rowset プロパティメソッドを呼び出して、ADO の Recordset オブジェクトの OLE DB Rowset オブジェクトを設定します。</span><span class="sxs-lookup"><span data-stu-id="37b71-124">Call the IADORecordsetConstruction::put\_Rowset property method to set the OLE DB Rowset object on the ADO Recordset object:</span></span>

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
<span data-ttu-id="37b71-125">これで、結果オブジェクトは、OLE DB **Rowset**オブジェクトから作成された ADO **Recordset**オブジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="37b71-125">The resultant object now represents the ADO **Recordset** object constructed from the OLE DB **Rowset** object.</span></span>

<span data-ttu-id="37b71-126">ADO **Recordset** オブジェクトは、OLE DB **Chapter** または **RowPosition** オブジェクトから作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="37b71-126">You can also construct an ADO **Recordset** object from an OLE DB **Chapter** or **RowPosition** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="37b71-127">要件</span><span class="sxs-lookup"><span data-stu-id="37b71-127">Requirements</span></span>

- <span data-ttu-id="37b71-128">**バージョン:** ADO 2.0 以上</span><span class="sxs-lookup"><span data-stu-id="37b71-128">**Version:** ADO 2.0 and later</span></span>

- <span data-ttu-id="37b71-129">**ライブラリ:** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="37b71-129">**Library:** msado15.dll</span></span>

- <span data-ttu-id="37b71-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="37b71-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span></span>

