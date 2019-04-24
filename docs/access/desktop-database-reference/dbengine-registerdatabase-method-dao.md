---
title: DBEngine データベースメソッド (DAO)
TOCTitle: RegisterDatabase Method
ms:assetid: ed87a694-2c89-0a78-5d8b-0cc7e09fadff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836347(v=office.15)
ms:contentKeyID: 48548541
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052938
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 632f6e10d79d74dfef295b34a52ce62f1690101b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294226"
---
# <a name="dbengineregisterdatabase-method-dao"></a><span data-ttu-id="c758f-102">DBEngine データベースメソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="c758f-102">DBEngine.RegisterDatabase method (DAO)</span></span>

<span data-ttu-id="c758f-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c758f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c758f-p101">ODBC データ ソースの接続情報を Windows レジストリに追加します。ODBC ドライバーでは、セッション中に ODBC データ ソースが開かれるときに、接続情報が必要になります。</span><span class="sxs-lookup"><span data-stu-id="c758f-p101">Enters connection information for an ODBC data source in the Windows Registry. The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="c758f-106">構文</span><span class="sxs-lookup"><span data-stu-id="c758f-106">Syntax</span></span>

<span data-ttu-id="c758f-107">*式*。registerdatabase (***Dsn***、***ドライバー***、***サイレント***、***属性***)</span><span class="sxs-lookup"><span data-stu-id="c758f-107">*expression* .RegisterDatabase(***Dsn***, ***Driver***, ***Silent***, ***Attributes***)</span></span>

<span data-ttu-id="c758f-108">\*式\***DBEngine**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="c758f-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="c758f-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c758f-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c758f-110">名前</span><span class="sxs-lookup"><span data-stu-id="c758f-110">Name</span></span></p></th>
<th><p><span data-ttu-id="c758f-111">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="c758f-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="c758f-112">データ型</span><span class="sxs-lookup"><span data-stu-id="c758f-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="c758f-113">説明</span><span class="sxs-lookup"><span data-stu-id="c758f-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c758f-114"><em>代わりに</em></span><span class="sxs-lookup"><span data-stu-id="c758f-114"><em>Dsn</em></span></span></p></td>
<td><p><span data-ttu-id="c758f-115">必須</span><span class="sxs-lookup"><span data-stu-id="c758f-115">Required</span></span></p></td>
<td><p><span data-ttu-id="c758f-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="c758f-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="c758f-117"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong>メソッドで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="c758f-117">the name used in the <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> method.</span></span> <span data-ttu-id="c758f-118">データ ソースに関する説明的な情報を指します。</span><span class="sxs-lookup"><span data-stu-id="c758f-118">It refers to a block of descriptive information about the data source.</span></span> <span data-ttu-id="c758f-119">たとえば、データ ソースが ODBC リモート データベースである場合は、サーバー名などを指定します。</span><span class="sxs-lookup"><span data-stu-id="c758f-119">For example, if the data source is an ODBC remote database, it could be the name of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c758f-120"><em>Driver</em></span><span class="sxs-lookup"><span data-stu-id="c758f-120"><em>Driver</em></span></span></p></td>
<td><p><span data-ttu-id="c758f-121">必須</span><span class="sxs-lookup"><span data-stu-id="c758f-121">Required</span></span></p></td>
<td><p><span data-ttu-id="c758f-122"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="c758f-122"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="c758f-123">ODBC ドライバーの名前です。</span><span class="sxs-lookup"><span data-stu-id="c758f-123">The name of the ODBC driver.</span></span> <span data-ttu-id="c758f-124">ODBC ドライバーの DLL ファイルの名前ではありません。</span><span class="sxs-lookup"><span data-stu-id="c758f-124">This isn't the name of the ODBC driver DLL file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c758f-125"><em>静寂</em></span><span class="sxs-lookup"><span data-stu-id="c758f-125"><em>Silent</em></span></span></p></td>
<td><p><span data-ttu-id="c758f-126">必須</span><span class="sxs-lookup"><span data-stu-id="c758f-126">Required</span></span></p></td>
<td><p><span data-ttu-id="c758f-127"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="c758f-127"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="c758f-128">ドライバー固有の情報の入力を求める ODBC ドライバー ダイアログ ボックスを表示しない場合は <strong>True</strong>、表示する場合は <strong>False</strong> に設定します。</span><span class="sxs-lookup"><span data-stu-id="c758f-128"><strong>True</strong> if you don't want to display the ODBC driver dialog boxes that prompt for driver-specific information; or <strong>False</strong> if you want to display the ODBC driver dialog boxes.</span></span> <span data-ttu-id="c758f-129">silent に<strong>True</strong>が設定されている場合、属性に必要なドライバー固有の情報がすべて含まれている必要があります。または、ダイアログボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c758f-129">If silent is <strong>True</strong>, attributes must contain all the necessary driver-specific information or the dialog boxes are displayed anyway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c758f-130"><em>属性</em></span><span class="sxs-lookup"><span data-stu-id="c758f-130"><em>Attributes</em></span></span></p></td>
<td><p><span data-ttu-id="c758f-131">必須</span><span class="sxs-lookup"><span data-stu-id="c758f-131">Required</span></span></p></td>
<td><p><span data-ttu-id="c758f-132"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="c758f-132"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="c758f-133">Windows レジストリに追加するキーワードの一覧です。</span><span class="sxs-lookup"><span data-stu-id="c758f-133">A list of keywords to be added to the Windows Registry.</span></span> <span data-ttu-id="c758f-134">キーワードは、改行で区切られた文字列として指定します。</span><span class="sxs-lookup"><span data-stu-id="c758f-134">The keywords are in a carriage-return–delimited string.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c758f-135">注釈</span><span class="sxs-lookup"><span data-stu-id="c758f-135">Remarks</span></span>

<span data-ttu-id="c758f-136">**RegisterDatabase** メソッドを使用した時点で、データベースが既に Windows レジストリに登録されている (接続情報が既に追加されている) 場合は、その接続情報が更新されます。</span><span class="sxs-lookup"><span data-stu-id="c758f-136">If the database is already registered (connection information is already entered) in the Windows Registry when you use the **RegisterDatabase** method, the connection information is updated.</span></span>

<span data-ttu-id="c758f-137">**RegisterDatabase** メソッドがなんらかの理由で失敗すると、Windows レジストリは変更されず、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="c758f-137">If the **RegisterDatabase** method fails for any reason, no changes are made to the Windows Registry, and an error occurs.</span></span>

<span data-ttu-id="c758f-138">SQL Server など ODBC ドライバーの詳細については、ドライバーに付属のヘルプ ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="c758f-138">For more information about ODBC drivers such as SQL Server, see the Help file provided with the driver.</span></span>

## <a name="example"></a><span data-ttu-id="c758f-139">例</span><span class="sxs-lookup"><span data-stu-id="c758f-139">Example</span></span>

<span data-ttu-id="c758f-140">次の例では、 **RegisterDatabase** メソッドを使用して、Publishers という名前の Microsoft SQL Server データ ソースを Windows レジストリに登録します。</span><span class="sxs-lookup"><span data-stu-id="c758f-140">This example uses the **RegisterDatabase** method to register a Microsoft SQL Server data source named Publishers in the Windows Registry.</span></span>

```vb 
Sub RegisterDatabaseX() 
 
 Dim dbsRegister As Database 
 Dim strDescription As String 
 Dim strAttributes As String 
 Dim errLoop As Error 
 
 ' Build keywords string. 
 strDescription = InputBox( "Enter a description " & _ 
 "for the database to be registered.") 
 strAttributes = "Database=pubs" & _ 
 vbCr & "Description=" & strDescription & _ 
 vbCr & "OemToAnsi=No" & _ 
 vbCr & "Server=Server1" 
 
 ' Update Windows Registry. 
 On Error GoTo Err_Register 
 DBEngine.RegisterDatabase "Publishers", "SQL Server", _ 
 True, strAttributes 
 On Error GoTo 0 
 
 MsgBox "Use regedit.exe to view changes: " & _ 
 "HKEY_CURRENT_USER\" & _ 
 "Software\ODBC\ODBC.INI" 
 
 Exit Sub 
 
Err_Register: 
 
 ' Notify user of any errors that result from 
 ' the invalid data. 
 If DBEngine.Errors.Count > 0 Then 
 For Each errLoop In DBEngine.Errors 
 MsgBox "Error number: " & errLoop.Number & _ 
 vbCr & errLoop.Description 
 Next errLoop 
 End If 
 
 Resume Next 
 
End Sub 
 
```

