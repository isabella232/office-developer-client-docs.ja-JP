---
title: Field2.LoadFromFile メソッド (DAO)
TOCTitle: LoadFromFile Method
ms:assetid: 8ffe4636-d4da-0579-f4b5-14f423647562
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197396(v=office.15)
ms:contentKeyID: 48546314
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101190
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c7780520f70b418b8fa6865ef3b85f50be132ee7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477176"
---
# <a name="field2loadfromfile-method-dao"></a><span data-ttu-id="5b316-102">Field2.LoadFromFile メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="5b316-102">Field2.LoadFromFile Method (DAO)</span></span>

<span data-ttu-id="5b316-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5b316-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5b316-104">指定されたファイルをディスクから読み込みます。</span><span class="sxs-lookup"><span data-stu-id="5b316-104">Loads the specified file from disk.</span></span>

## <a name="version-information"></a><span data-ttu-id="5b316-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="5b316-105">Version Information</span></span>

<span data-ttu-id="5b316-106">追加バージョン: Access 2007</span><span class="sxs-lookup"><span data-stu-id="5b316-106">Version Added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="5b316-107">構文</span><span class="sxs-lookup"><span data-stu-id="5b316-107">Syntax</span></span>

<span data-ttu-id="5b316-108">*式*です。LoadFromFile (***ファイル名***)</span><span class="sxs-lookup"><span data-stu-id="5b316-108">*expression* .LoadFromFile(***FileName***)</span></span>

<span data-ttu-id="5b316-109">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="5b316-109">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="5b316-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5b316-110">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5b316-111">名前</span><span class="sxs-lookup"><span data-stu-id="5b316-111">Name</span></span></p></th>
<th><p><span data-ttu-id="5b316-112">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="5b316-112">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="5b316-113">データ型</span><span class="sxs-lookup"><span data-stu-id="5b316-113">Data Type</span></span></p></th>
<th><p><span data-ttu-id="5b316-114">説明</span><span class="sxs-lookup"><span data-stu-id="5b316-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5b316-115">FileName</span><span class="sxs-lookup"><span data-stu-id="5b316-115">FileName</span></span></p></td>
<td><p><span data-ttu-id="5b316-116">必須</span><span class="sxs-lookup"><span data-stu-id="5b316-116">Required</span></span></p></td>
<td><p><span data-ttu-id="5b316-117"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="5b316-117"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="5b316-118">読み込むファイルの完全修飾パスです。</span><span class="sxs-lookup"><span data-stu-id="5b316-118">The fully qualified path of the file to that you want to load.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="5b316-119">例</span><span class="sxs-lookup"><span data-stu-id="5b316-119">Example</span></span>

<span data-ttu-id="5b316-120">次のコードでは、 **LoadFromFile** メソッドを使用して、社員の画像をディスクから読み込みます。</span><span class="sxs-lookup"><span data-stu-id="5b316-120">The following code snippet uses the **LoadFromFile** method to load an employee's picture from disk.</span></span>

```vb 
   '  Instantiate the parent recordset.  
   Set rsEmployees = db.OpenRecordset("Employees") 
  
   … Code to move to desired employee 
  
   ' Activate edit mode. 
   rsEmployees.Edit 
  
   ' Instantiate the child recordset. 
   Set rsPictures = rsEmployees.Fields("Pictures").Value  
  
   ' Add a new attachment. 
   rsPictures.AddNew 
   rsPictures.Fields("FileData").LoadFromFile "EmpPhoto39392.jpg" 
   rsPictures.Update 
  
   ' Update the parent record 
   rsEmployees.Update 
```

<br/>

<span data-ttu-id="5b316-121">次の例は、指定されたフォルダー パスから添付ファイル型フィールドにファイルを追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5b316-121">The following example shows how to add files from a specified folder path to an attachment field.</span></span>

<span data-ttu-id="5b316-122">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="5b316-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Public Function LoadAttachments(strPath As String, Optional strPattern As String = "*.*") As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld  As DAO.Field2
        Dim strFile As String
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Load all attachments in the specified directory
            strFile = Dir(strPath & "\*.*")
            
            rst.Edit
            Do While Len(strFile) > 0
                'Add a new attachment that matches the pattern.
                'Pass "" to match all files.
                If strFile Like strPattern Then
                    rsA.AddNew
                    rsA("FileData").LoadFromFile strPath & "\" & strFile
                    rsA.Update
                    
                    'Increment the number of files added
                    LoadAttachments = LoadAttachments + 1
                End If
                strFile = Dir
            Loop
            rsA.Close
            
            rst.Update
            'Next record
            rst.MoveNext
        Loop
        
        rst.Close
        dbs.Close
        
        Set fld = Nothing
        Set rsA = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Function
```