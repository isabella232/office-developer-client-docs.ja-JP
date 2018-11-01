---
title: Field2.SaveToFile メソッド (DAO)
TOCTitle: SaveToFile Method
ms:assetid: 250f9596-1a03-471d-96f9-718cd57dc94f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191852(v=office.15)
ms:contentKeyID: 48543776
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101191
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bdcd5f0d4d131533846eb4c05d2579f0703d408d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875711"
---
# <a name="field2savetofile-method-dao"></a><span data-ttu-id="28aec-102">Field2.SaveToFile メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="28aec-102">Field2.SaveToFile Method (DAO)</span></span>

<span data-ttu-id="28aec-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="28aec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28aec-104">ディスクに添付ファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="28aec-104">Saves an attachment to disk.</span></span>

## <a name="version-information"></a><span data-ttu-id="28aec-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="28aec-105">Version Information</span></span>

<span data-ttu-id="28aec-106">追加バージョン: Access 2007</span><span class="sxs-lookup"><span data-stu-id="28aec-106">Version Added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="28aec-107">構文</span><span class="sxs-lookup"><span data-stu-id="28aec-107">Syntax</span></span>

<span data-ttu-id="28aec-108">*式*です。SaveToFile (***ファイル名***)</span><span class="sxs-lookup"><span data-stu-id="28aec-108">*expression* .SaveToFile(***FileName***)</span></span>

<span data-ttu-id="28aec-109">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="28aec-109">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="28aec-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="28aec-110">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="28aec-111">名前</span><span class="sxs-lookup"><span data-stu-id="28aec-111">Name</span></span></p></th>
<th><p><span data-ttu-id="28aec-112">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="28aec-112">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="28aec-113">データ型</span><span class="sxs-lookup"><span data-stu-id="28aec-113">Data Type</span></span></p></th>
<th><p><span data-ttu-id="28aec-114">説明</span><span class="sxs-lookup"><span data-stu-id="28aec-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="28aec-115">FileName</span><span class="sxs-lookup"><span data-stu-id="28aec-115">FileName</span></span></p></td>
<td><p><span data-ttu-id="28aec-116">必須</span><span class="sxs-lookup"><span data-stu-id="28aec-116">Required</span></span></p></td>
<td><p><span data-ttu-id="28aec-117"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="28aec-117"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="28aec-118">添付ファイルを保存するファイルの完全修飾パスです。</span><span class="sxs-lookup"><span data-stu-id="28aec-118">The fully qualified path of the file to which you want to save the attachment.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="28aec-119">例</span><span class="sxs-lookup"><span data-stu-id="28aec-119">Example</span></span>

<span data-ttu-id="28aec-120">次のコードは、 **SaveToFile** メソッドを使用して、特定の社員に関するすべての添付ファイルをディスクに保存する方法の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="28aec-120">The following code snippet illustrates how to use the **SaveToFile** method to save all of the attachments for a specific employee to disk.</span></span>

```vb
    '  Instantiate the parent recordset.  
       Set rsEmployees = db.OpenRecordset("Employees") 
      
       … Code to move to desired employee 
      
       ' Instantiate the child recordset. 
       Set rsPictures = rsEmployees.Fields("Pictures").Value  
     
       '  Loop through the attachments. 
       While Not rsPictures.EOF 
      
          '  Save current attachment to disk in the "My Documents" folder. 
          rsPictures.Fields("FileData").SaveToFile _ 
                      "C:\Documents and Settings\Username\My Documents" 
          rsPictures.MoveNext 
       Wend 
```

<br/>

<span data-ttu-id="28aec-121">次の例は、添付ファイル型フィールドに保管されているファイルを、指定されたフォルダー パスに保存する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="28aec-121">The following example shows how to save the files stored in an attachment field to the specified folder path.</span></span>

<span data-ttu-id="28aec-122">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="28aec-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Public Function SaveAttachments(strPath As String, Optional strPattern As String = "*.*") As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        Dim strFullPath As String
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Save all attachments in the field
            Do While Not rsA.EOF
                If rsA("FileName") Like strPattern Then
                    strFullPath = strPath & "\" & rsA("FileName")
                    
                    'Make sure the file does not exist and save
                    If Dir(strFullPath) = "" Then
                        rsA("FileData").SaveToFile strFullPath
                    End If
                    
                    'Increment the number of files saved
                    SaveAttachments = SaveAttachments + 1
                End If
                
                'Next attachment
                rsA.MoveNext
            Loop
            rsA.Close
            
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
