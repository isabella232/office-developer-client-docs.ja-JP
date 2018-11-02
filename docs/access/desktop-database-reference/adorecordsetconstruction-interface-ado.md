---
title: ADORecordsetConstruction インターフェイス (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8ab9723d3acc698aa36210e26e370c0edfa67728
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924233"
---
# <a name="adorecordsetconstruction-interface-ado"></a><span data-ttu-id="97e92-102">ADORecordsetConstruction インターフェイス (ADO)</span><span class="sxs-lookup"><span data-stu-id="97e92-102">ADORecordsetConstruction interface (ADO)</span></span>


<span data-ttu-id="97e92-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="97e92-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97e92-104">. **ADORecordsetConstruction** インターフェイスは、C/C++ アプリケーションで OLE DB **Rowset** オブジェクトから ADO **Recordset** オブジェクトを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="97e92-104">The **ADORecordsetConstruction** interface is used to construct an ADO **Recordset** object from an OLE DB **Rowset** object in a C/C++ application.</span></span>

<span data-ttu-id="97e92-105">このインターフェイスでは、以下のプロパティがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="97e92-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="97e92-106">プロパティ</span><span class="sxs-lookup"><span data-stu-id="97e92-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97e92-107"><a href="chapter-property-ado.md">章</a></span><span class="sxs-lookup"><span data-stu-id="97e92-107"><a href="chapter-property-ado.md">Chapter</a></span></span></p></td>
<td><p><span data-ttu-id="97e92-108">読み取り/書き込み。</span><span class="sxs-lookup"><span data-stu-id="97e92-108">Read/Write.</span></span><br />
<span data-ttu-id="97e92-109"><strong>章</strong>の OLE DB オブジェクトから/この ADO<strong>レコード セット</strong>オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="97e92-109">Gets/sets an OLE DB <strong>Chapter</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97e92-110"><a href="rowposition-property-ado.md">RowPosition</a></span><span class="sxs-lookup"><span data-stu-id="97e92-110"><a href="rowposition-property-ado.md">RowPosition</a></span></span></p></td>
<td><p><span data-ttu-id="97e92-111">読み取り/書き込み。</span><span class="sxs-lookup"><span data-stu-id="97e92-111">Read/Write.</span></span><br />
<span data-ttu-id="97e92-112">OLE DB <strong>RowPosition</strong>オブジェクトから/この ADO<strong>レコード セット</strong>オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="97e92-112">Gets/sets an OLE DB <strong>RowPosition</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97e92-113"><a href="rowset-property-ado.md">行セット</a></span><span class="sxs-lookup"><span data-stu-id="97e92-113"><a href="rowset-property-ado.md">Rowset</a></span></span></p></td>
<td><p><span data-ttu-id="97e92-114">読み取り/書き込み。</span><span class="sxs-lookup"><span data-stu-id="97e92-114">Read/Write.</span></span><br />
<span data-ttu-id="97e92-115">/に ADO<strong>レコード セット</strong>オブジェクトには、OLE DB<strong>行セット</strong>オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="97e92-115">Gets/sets an OLE DB <strong>Rowset</strong> object from/on this ADO <strong>Recordset</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="97e92-116">メソッド</span><span class="sxs-lookup"><span data-stu-id="97e92-116">Methods</span></span>

<span data-ttu-id="97e92-117">なし</span><span class="sxs-lookup"><span data-stu-id="97e92-117">None.</span></span>

## <a name="events"></a><span data-ttu-id="97e92-118">イベント</span><span class="sxs-lookup"><span data-stu-id="97e92-118">Events</span></span>

<span data-ttu-id="97e92-119">なし</span><span class="sxs-lookup"><span data-stu-id="97e92-119">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="97e92-120">備考</span><span class="sxs-lookup"><span data-stu-id="97e92-120">Remarks</span></span>

<span data-ttu-id="97e92-121">次の 3 つの基本的な操作を OLE DB の**行セット**オブジェクトのため、ADO**レコード セット**オブジェクトの () の構築、ADO**レコード セット**のオブジェクト (どちら) 金額の構築を指定します。</span><span class="sxs-lookup"><span data-stu-id="97e92-121">Given an OLE DB **Rowset** object (pRowset ), the construction of an ADO **Recordset** object (), the construction of an ADO **Recordset** object (adoRs ) amounts to the following three basic operations:</span></span>

1. <span data-ttu-id="97e92-122">ADO **Recordset** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="97e92-122">Create an ADO **Recordset** object:</span></span>
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. <span data-ttu-id="97e92-123">**IADORecordsetConstruction** インターフェイスで **Recordset** オブジェクトを照会します。</span><span class="sxs-lookup"><span data-stu-id="97e92-123">Query the **IADORecordsetConstruction** interface on the **Recordset** object:</span></span>

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. <span data-ttu-id="97e92-124">IADORecordsetConstruction::put を呼び出す\_ADO レコード セット オブジェクトの OLE DB 行セット オブジェクトを設定するのには行セット プロパティのメソッド。</span><span class="sxs-lookup"><span data-stu-id="97e92-124">Call the IADORecordsetConstruction::put\_Rowset property method to set the OLE DB Rowset object on the ADO Recordset object:</span></span>

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
<span data-ttu-id="97e92-125">これで、結果のオブジェクトは、OLE DB**行セット**オブジェクトから作成された ADO**レコード セット**オブジェクトを表します。</span><span class="sxs-lookup"><span data-stu-id="97e92-125">The resultant object now represents the ADO **Recordset** object constructed from the OLE DB **Rowset** object.</span></span>

<span data-ttu-id="97e92-126">ADO **Recordset** オブジェクトは、OLE DB **Chapter** または **RowPosition** オブジェクトから作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="97e92-126">You can also construct an ADO **Recordset** object from an OLE DB **Chapter** or **RowPosition** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="97e92-127">必要条件</span><span class="sxs-lookup"><span data-stu-id="97e92-127">Requirements</span></span>

- <span data-ttu-id="97e92-128">**バージョン:** ADO 2.0 以上</span><span class="sxs-lookup"><span data-stu-id="97e92-128">**Version:** ADO 2.0 and later</span></span>

- <span data-ttu-id="97e92-129">**ライブラリ:** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="97e92-129">**Library:** msado15.dll</span></span>

- <span data-ttu-id="97e92-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="97e92-130">**UUID:** 00000283-0000-0010-8000-00AA006D2EA4</span></span>

