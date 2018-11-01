---
title: DBEngine.RegisterDatabase メソッド (DAO)
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
ms.openlocfilehash: fcb8e675f488c0d69f4c0d0b6329c47085d51e26
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888623"
---
# <a name="dbengineregisterdatabase-method-dao"></a><span data-ttu-id="cef32-102">DBEngine.RegisterDatabase メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="cef32-102">DBEngine.RegisterDatabase Method (DAO)</span></span>


<span data-ttu-id="cef32-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cef32-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="cef32-p101">ODBC データ ソースの接続情報を Windows レジストリに追加します。ODBC ドライバーでは、セッション中に ODBC データ ソースが開かれるときに、接続情報が必要になります。</span><span class="sxs-lookup"><span data-stu-id="cef32-p101">Enters connection information for an ODBC data source in the Windows Registry. The ODBC driver needs connection information when the ODBC data source is opened during a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="cef32-106">構文</span><span class="sxs-lookup"><span data-stu-id="cef32-106">Syntax</span></span>

<span data-ttu-id="cef32-107">*式*です。RegisterDatabase (***Dsn\*\*\*\*\*\*ドライバー***、***サイレント***、***属性***)</span><span class="sxs-lookup"><span data-stu-id="cef32-107">*expression* .RegisterDatabase(***Dsn***, ***Driver***, ***Silent***, ***Attributes***)</span></span>

<span data-ttu-id="cef32-108">\*式\***DBEngine**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="cef32-108">*expression* A variable that represents a **DBEngine** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="cef32-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cef32-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cef32-110">名前</span><span class="sxs-lookup"><span data-stu-id="cef32-110">Name</span></span></p></th>
<th><p><span data-ttu-id="cef32-111">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="cef32-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="cef32-112">データ型</span><span class="sxs-lookup"><span data-stu-id="cef32-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="cef32-113">説明</span><span class="sxs-lookup"><span data-stu-id="cef32-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cef32-114">Dsn</span><span class="sxs-lookup"><span data-stu-id="cef32-114">Dsn</span></span></p></td>
<td><p><span data-ttu-id="cef32-115">必須</span><span class="sxs-lookup"><span data-stu-id="cef32-115">Required</span></span></p></td>
<td><p><span data-ttu-id="cef32-116"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="cef32-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="cef32-p102"><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> メソッドで使用される名前です。データ ソースに関する説明的な情報を指します。たとえば、データ ソースが ODBC リモート データベースである場合は、サーバー名などを指定します。</span><span class="sxs-lookup"><span data-stu-id="cef32-p102">the name used in the <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> method. It refers to a block of descriptive information about the data source. For example, if the data source is an ODBC remote database, it could be the name of the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cef32-120">ドライバー</span><span class="sxs-lookup"><span data-stu-id="cef32-120">Driver</span></span></p></td>
<td><p><span data-ttu-id="cef32-121">必須</span><span class="sxs-lookup"><span data-stu-id="cef32-121">Required</span></span></p></td>
<td><p><span data-ttu-id="cef32-122"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="cef32-122"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="cef32-p103">ODBC ドライバーの名前です。ODBC ドライバーの DLL ファイルの名前ではありません。</span><span class="sxs-lookup"><span data-stu-id="cef32-p103">The name of the ODBC driver. This isn't the name of the ODBC driver DLL file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cef32-125">サイレント</span><span class="sxs-lookup"><span data-stu-id="cef32-125">Silent</span></span></p></td>
<td><p><span data-ttu-id="cef32-126">必須</span><span class="sxs-lookup"><span data-stu-id="cef32-126">Required</span></span></p></td>
<td><p><span data-ttu-id="cef32-127"><strong>ブール型 (Boolean)</strong></span><span class="sxs-lookup"><span data-stu-id="cef32-127"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="cef32-128"><strong>True の</strong>場合、ドライバー固有の情報の入力を求める ODBC ドライバー ダイアログ ボックスを表示したくないです。または、 <strong>false を指定</strong>する場合は、ODBC ドライバーのダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="cef32-128"><strong>True</strong> if you don't want to display the ODBC driver dialog boxes that prompt for driver-specific information; or <strong>False</strong> if you want to display the ODBC driver dialog boxes.</span></span> <span data-ttu-id="cef32-129">場合<strong>はサイレント</strong>、属性には、必要なすべてのドライバー固有の情報が含まれている必要があります、またはダイアログ ボックスが表示されますか。</span><span class="sxs-lookup"><span data-stu-id="cef32-129">If silent is <strong>True</strong>, attributes must contain all the necessary driver-specific information or the dialog boxes are displayed anyway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cef32-130">属性</span><span class="sxs-lookup"><span data-stu-id="cef32-130">Attributes</span></span></p></td>
<td><p><span data-ttu-id="cef32-131">必須</span><span class="sxs-lookup"><span data-stu-id="cef32-131">Required</span></span></p></td>
<td><p><span data-ttu-id="cef32-132"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="cef32-132"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="cef32-p105">Windows レジストリに追加するキーワードの一覧です。キーワードは、改行で区切られた文字列として指定します。</span><span class="sxs-lookup"><span data-stu-id="cef32-p105">A list of keywords to be added to the Windows Registry. The keywords are in a carriage-return–delimited string.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="cef32-135">注釈</span><span class="sxs-lookup"><span data-stu-id="cef32-135">Remarks</span></span>

<span data-ttu-id="cef32-136">**RegisterDatabase** メソッドを使用した時点で、データベースが既に Windows レジストリに登録されている (接続情報が既に追加されている) 場合は、その接続情報が更新されます。</span><span class="sxs-lookup"><span data-stu-id="cef32-136">If the database is already registered (connection information is already entered) in the Windows Registry when you use the **RegisterDatabase** method, the connection information is updated.</span></span>

<span data-ttu-id="cef32-137">**RegisterDatabase** メソッドがなんらかの理由で失敗すると、Windows レジストリは変更されず、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="cef32-137">If the **RegisterDatabase** method fails for any reason, no changes are made to the Windows Registry, and an error occurs.</span></span>

<span data-ttu-id="cef32-138">SQL Server など ODBC ドライバーの詳細については、ドライバーに付属のヘルプ ファイルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cef32-138">For more information about ODBC drivers such as SQL Server, see the Help file provided with the driver.</span></span>

## <a name="example"></a><span data-ttu-id="cef32-139">例</span><span class="sxs-lookup"><span data-stu-id="cef32-139">Example</span></span>

<span data-ttu-id="cef32-140">次の例では、 **RegisterDatabase** メソッドを使用して、Publishers という名前の Microsoft SQL Server データ ソースを Windows レジストリに登録します。</span><span class="sxs-lookup"><span data-stu-id="cef32-140">This example uses the **RegisterDatabase** method to register a Microsoft SQL Server data source named Publishers in the Windows Registry.</span></span>

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

