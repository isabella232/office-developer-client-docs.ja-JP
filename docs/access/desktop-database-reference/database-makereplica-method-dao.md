---
title: Database.MakeReplica メソッド (DAO)
TOCTitle: MakeReplica Method
ms:assetid: b6bf4982-0804-12ce-849f-d2b4ac2e48a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822413(v=office.15)
ms:contentKeyID: 48547286
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053371
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 632bf0af35dd49951d58ba126b6e03678a1a12db
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950252"
---
# <a name="databasemakereplica-method-dao"></a><span data-ttu-id="6cc6a-102">Database.MakeReplica メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="6cc6a-102">Database.MakeReplica method (DAO)</span></span>

<span data-ttu-id="6cc6a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6cc6a-104">データベースの別のレプリカから新しいレプリカを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-104">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="6cc6a-105">構文</span><span class="sxs-lookup"><span data-stu-id="6cc6a-105">Syntax</span></span>

<span data-ttu-id="6cc6a-106">*式*です。MakeReplica (***パス名***、***説明***、***オプション***)</span><span class="sxs-lookup"><span data-stu-id="6cc6a-106">*expression* .MakeReplica(***PathName***, ***Description***, ***Options***)</span></span>

<span data-ttu-id="6cc6a-107">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="6cc6a-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6cc6a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6cc6a-109">名前</span><span class="sxs-lookup"><span data-stu-id="6cc6a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="6cc6a-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="6cc6a-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="6cc6a-111">データ型</span><span class="sxs-lookup"><span data-stu-id="6cc6a-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="6cc6a-112">説明</span><span class="sxs-lookup"><span data-stu-id="6cc6a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cc6a-113"><em>パス名</em></span><span class="sxs-lookup"><span data-stu-id="6cc6a-113"><em>PathName</em></span></span></p></td>
<td><p><span data-ttu-id="6cc6a-114">必須</span><span class="sxs-lookup"><span data-stu-id="6cc6a-114">Required</span></span></p></td>
<td><p><span data-ttu-id="6cc6a-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="6cc6a-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc6a-p101">新しいレプリカのパスおよびファイル名。レプリカの名前として既存のファイル名を指定すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-p101">The path and file name of the new replica. If replica is an existing file name, then an error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cc6a-118"><em>説明</em></span><span class="sxs-lookup"><span data-stu-id="6cc6a-118"><em>Description</em></span></span></p></td>
<td><p><span data-ttu-id="6cc6a-119">必須</span><span class="sxs-lookup"><span data-stu-id="6cc6a-119">Required</span></span></p></td>
<td><p><span data-ttu-id="6cc6a-120"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="6cc6a-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc6a-121">作成するレプリカの説明を表す文字列型 (<strong>String</strong>) の値。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-121">A <strong>String</strong> that describes the replica that you are creating</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cc6a-122"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="6cc6a-122"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="6cc6a-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="6cc6a-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="6cc6a-124"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="6cc6a-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="6cc6a-125">作成するレプリカの特性を指定する<strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong>クラスの定数を取得します。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-125">A <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> constant that specifies characteristics of the replica you are creating.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="6cc6a-126">注釈</span><span class="sxs-lookup"><span data-stu-id="6cc6a-126">Remarks</span></span>

<span data-ttu-id="6cc6a-127">新しく作成した部分レプリカの **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** のすべてのプロパティは、テーブルにデータがないことを示す **False** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-127">A newly created partial replica will have all **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** properties set to **False**, meaning that no data will be in the tables.</span></span>

## <a name="example"></a><span data-ttu-id="6cc6a-128">例</span><span class="sxs-lookup"><span data-stu-id="6cc6a-128">Example</span></span>

<span data-ttu-id="6cc6a-129">次の使用例では、 **MakeReplica** メソッドを使用して、既存のデザイン マスターの新しいレプリカを作成します。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span></span> <span data-ttu-id="6cc6a-130">IntOptions 引数は、定数**dbRepMakeReadOnly**と**dbRepMakePartial**の組み合わせ、または 0 であることができます。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-130">The intOptions argument can be a combination of the constants **dbRepMakeReadOnly** and **dbRepMakePartial**, or it can be 0.</span></span> <span data-ttu-id="6cc6a-131">たとえば、読み取り専用の部分的なレプリカを作成するにして渡す必要があります値**dbRepMakeReadOnly** + intOptions の値として**dbRepMakePartial** 。</span><span class="sxs-lookup"><span data-stu-id="6cc6a-131">For example, to create a read-only partial replica, you should pass the value **dbRepMakeReadOnly** + **dbRepMakePartial** as the value of intOptions.</span></span>

```vb 
Function MakeAdditionalReplica(strReplicableDB As _ 
 String, strNewReplica As String, intOptions As _ 
 Integer) As Integer 
 
 Dim dbsTemp As Database 
 On Error GoTo ErrorHandler 
 
 Set dbsTemp = OpenDatabase(strReplicableDB) 
 
 ' If no options are passed to 
 ' MakeAdditionalReplica, omit the 
 ' options argument, which defaults to 
 ' a full, read/write replica. Otherwise, 
 ' use the value of intOptions. 
 
 If intOptions = 0 Then 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB 
 Else 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB, _ 
 intOptions 
 End If 
 
 dbsTemp.Close 
 
ErrorHandler: 
 Select Case Err 
 Case 0: 
 MakeAdditionalReplica = 0 
 Exit Function 
 Case Else: 
 MsgBox "Error " & Err & " : " & Error 
 MakeAdditionalReplica = Err 
 Exit Function 
 End Select 
 
End Function 
 
```

