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
localization_priority: Normal
ms.openlocfilehash: 9b9e2eac360d157f28b986b6598ade58b8c34ec6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711967"
---
# <a name="databasemakereplica-method-dao"></a><span data-ttu-id="7e7e7-102">Database.MakeReplica メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="7e7e7-102">Database.MakeReplica method (DAO)</span></span>

<span data-ttu-id="7e7e7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7e7e7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7e7e7-104">データベースの別のレプリカから新しいレプリカを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="7e7e7-104">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e7e7-105">構文</span><span class="sxs-lookup"><span data-stu-id="7e7e7-105">Syntax</span></span>

<span data-ttu-id="7e7e7-106">*式*です。MakeReplica (***パス名***、***説明***、***オプション***)</span><span class="sxs-lookup"><span data-stu-id="7e7e7-106">*expression* .MakeReplica(***PathName***, ***Description***, ***Options***)</span></span>

<span data-ttu-id="7e7e7-107">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="7e7e7-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7e7e7-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7e7e7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7e7e7-109">名前</span><span class="sxs-lookup"><span data-stu-id="7e7e7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7e7e7-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="7e7e7-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7e7e7-111">データ型</span><span class="sxs-lookup"><span data-stu-id="7e7e7-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="7e7e7-112">説明</span><span class="sxs-lookup"><span data-stu-id="7e7e7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7e7e7-113"><em>PathName</em></span><span class="sxs-lookup"><span data-stu-id="7e7e7-113"><em>PathName</em></span></span></p></td>
<td><p><span data-ttu-id="7e7e7-114">必須</span><span class="sxs-lookup"><span data-stu-id="7e7e7-114">Required</span></span></p></td>
<td><p><span data-ttu-id="7e7e7-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="7e7e7-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7e7e7-p101">新しいレプリカのパスおよびファイル名。レプリカの名前として既存のファイル名を指定すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7e7e7-p101">The path and file name of the new replica. If replica is an existing file name, then an error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7e7e7-118"><em>説明</em></span><span class="sxs-lookup"><span data-stu-id="7e7e7-118"><em>Description</em></span></span></p></td>
<td><p><span data-ttu-id="7e7e7-119">必須</span><span class="sxs-lookup"><span data-stu-id="7e7e7-119">Required</span></span></p></td>
<td><p><span data-ttu-id="7e7e7-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="7e7e7-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="7e7e7-121">作成するレプリカの説明を表す文字列型 (<strong>String</strong>) の値。</span><span class="sxs-lookup"><span data-stu-id="7e7e7-121">A <strong>String</strong> that describes the replica that you are creating</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7e7e7-122"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="7e7e7-122"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="7e7e7-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="7e7e7-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="7e7e7-124"><strong>Variant (バリアント型)</strong></span><span class="sxs-lookup"><span data-stu-id="7e7e7-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7e7e7-125">作成するレプリカの特性を指定する<strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong>クラスの定数を取得します。</span><span class="sxs-lookup"><span data-stu-id="7e7e7-125">A <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> constant that specifies characteristics of the replica you are creating.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7e7e7-126">注釈</span><span class="sxs-lookup"><span data-stu-id="7e7e7-126">Remarks</span></span>

<span data-ttu-id="7e7e7-127">新しく作成した部分レプリカの **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** のすべてのプロパティは、テーブルにデータがないことを示す **False** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7e7e7-127">A newly created partial replica will have all **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** properties set to **False**, meaning that no data will be in the tables.</span></span>

## <a name="example"></a><span data-ttu-id="7e7e7-128">例</span><span class="sxs-lookup"><span data-stu-id="7e7e7-128">Example</span></span>

<span data-ttu-id="7e7e7-129">次の使用例では、 **MakeReplica** メソッドを使用して、既存のデザイン マスターの新しいレプリカを作成します。</span><span class="sxs-lookup"><span data-stu-id="7e7e7-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span></span> <span data-ttu-id="7e7e7-130">IntOptions 引数は、定数**dbRepMakeReadOnly**と**dbRepMakePartial**の組み合わせ、または 0 であることができます。</span><span class="sxs-lookup"><span data-stu-id="7e7e7-130">The intOptions argument can be a combination of the constants **dbRepMakeReadOnly** and **dbRepMakePartial**, or it can be 0.</span></span> <span data-ttu-id="7e7e7-131">たとえば、読み取り専用の部分的なレプリカを作成するにして渡す必要があります値**dbRepMakeReadOnly** + intOptions の値として**dbRepMakePartial** 。</span><span class="sxs-lookup"><span data-stu-id="7e7e7-131">For example, to create a read-only partial replica, you should pass the value **dbRepMakeReadOnly** + **dbRepMakePartial** as the value of intOptions.</span></span>

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

