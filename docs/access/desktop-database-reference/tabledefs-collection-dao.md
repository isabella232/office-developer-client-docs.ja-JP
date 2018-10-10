---
title: TableDefs コレクション (DAO)
TOCTitle: TableDefs Collection
ms:assetid: a2986b02-0437-d6ac-7bbb-c43f5225c3fc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820997(v=office.15)
ms:contentKeyID: 48546766
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 084e11bf892a63d6b526e5f584de1ae450264c75
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479154"
---
# <a name="tabledefs-collection-dao"></a><span data-ttu-id="41c8f-102">TableDefs コレクション (DAO)</span><span class="sxs-lookup"><span data-stu-id="41c8f-102">TableDefs Collection (DAO)</span></span>

<span data-ttu-id="41c8f-103">**に適用されます:** Access 2013 |Office 2013</span><span class="sxs-lookup"><span data-stu-id="41c8f-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="41c8f-104">**TableDefs** コレクションには、データベースに格納されているすべての **TableDef** オブジェクトが含まれます (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="41c8f-104">A **TableDefs** collection contains all stored **TableDef** objects in a database (Microsoft Access workspaces only).</span></span>

## <a name="remarks"></a><span data-ttu-id="41c8f-105">注釈</span><span class="sxs-lookup"><span data-stu-id="41c8f-105">Remarks</span></span>

<span data-ttu-id="41c8f-106">テーブルの定義は、 **TableDef** オブジェクトおよびそのメソッドとプロパティを使用して操作します。</span><span class="sxs-lookup"><span data-stu-id="41c8f-106">You manipulate a table definition using a **TableDef** object and its methods and properties.</span></span>

<span data-ttu-id="41c8f-107">**Database** オブジェクトの既定のコレクションは、 **TableDefs** コレクションです。</span><span class="sxs-lookup"><span data-stu-id="41c8f-107">The default collection of a **Database** object is the **TableDefs** collection.</span></span>

<span data-ttu-id="41c8f-108">コレクション内の **TableDef** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="41c8f-108">To refer to a **TableDef** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

<span data-ttu-id="41c8f-109">**テーブル定義**(0)</span><span class="sxs-lookup"><span data-stu-id="41c8f-109">**TableDefs**(0)</span></span>

<span data-ttu-id="41c8f-110">**テーブル定義**("name")</span><span class="sxs-lookup"><span data-stu-id="41c8f-110">**TableDefs**("name")</span></span>

<span data-ttu-id="41c8f-111">**テーブル**\!\[名\]</span><span class="sxs-lookup"><span data-stu-id="41c8f-111">**TableDefs**\!\[name\]</span></span>

<span data-ttu-id="41c8f-112">**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。</span><span class="sxs-lookup"><span data-stu-id="41c8f-112">**Links provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="41c8f-113">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="41c8f-113">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

  - [<span data-ttu-id="41c8f-114">Re-Linker Multi-Backends</span><span class="sxs-lookup"><span data-stu-id="41c8f-114">Re-Linker Multi-Backends</span></span>](https://www.utteraccess.com/wiki/index.php/re-linker_multi-backends)

  - [<span data-ttu-id="41c8f-115">Swap/Relink Between LIVE, TEST and LOCAL Data</span><span class="sxs-lookup"><span data-stu-id="41c8f-115">Swap/Relink Between LIVE, TEST and LOCAL Data</span></span>](https://www.utteraccess.com/forum/swap-relink-live-test-t1328573.html)

## <a name="example"></a><span data-ttu-id="41c8f-116">例</span><span class="sxs-lookup"><span data-stu-id="41c8f-116">Example</span></span>

<span data-ttu-id="41c8f-p102">この例では、新しい **TableDef** オブジェクトを作成し、Northwind Database オブジェクトの **TableDefs** コレクションに追加します。次に、 **TableDefs** コレクションおよび新しい **TableDef** オブジェクトの **Properties** コレクションを列挙します。</span><span class="sxs-lookup"><span data-stu-id="41c8f-p102">This example creates a new **TableDef** object and appends it to the **TableDefs** collection of the Northwind Database object. It then enumerates the **TableDefs** collection and the **Properties** collection of the new **TableDef**.</span></span>

```vb
    Sub TableDefX() 
     
       Dim dbsNorthwind As Database 
       Dim tdfNew As TableDef 
       Dim tdfLoop As TableDef 
       Dim prpLoop As Property 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
       ' Create new TableDef object, append Field objects  
       ' to its Fields collection, and append TableDef  
       ' object to the TableDefs collection of the  
       ' Database object. 
       Set tdfNew = dbsNorthwind.CreateTableDef("NewTableDef") 
       tdfNew.Fields.Append tdfNew.CreateField("Date", dbDate) 
       dbsNorthwind.TableDefs.Append tdfNew 
     
       With dbsNorthwind 
          Debug.Print .TableDefs.Count & _ 
             " TableDefs in " & .Name 
     
          ' Enumerate TableDefs collection. 
          For Each tdfLoop In .TableDefs 
             Debug.Print "  " & tdfLoop.Name 
          Next tdfLoop 
     
          With tdfNew 
             Debug.Print "Properties of " & .Name 
     
             ' Enumerate Properties collection of new 
             ' TableDef object, only printing properties 
             ' with non-empty values. 
             For Each prpLoop In .Properties 
                Debug.Print "  " & prpLoop.Name & " - " & _ 
                   IIf(prpLoop = "", "[empty]", prpLoop) 
             Next prpLoop 
     
          End With 
     
          ' Delete new TableDef since this is a  
          ' demonstration. 
          .TableDefs.Delete tdfNew.Name 
          .Close 
       End With 
     
    End Sub 
```

<br/>

<span data-ttu-id="41c8f-119">この例では、Northwind データベースで新しい **TableDef** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="41c8f-119">This example creates a new **TableDef** object in the Northwind database.</span></span>

```vb 
Sub CreateTableDefX() 
 
   Dim dbsNorthwind As Database 
   Dim tdfNew As TableDef 
   Dim prpLoop As Property 
 
   Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
   ' Create a new TableDef object. 
   Set tdfNew = dbsNorthwind.CreateTableDef("Contacts") 
 
   With tdfNew 
      ' Create fields and append them to the new TableDef  
      ' object. This must be done before appending the  
      ' TableDef object to the TableDefs collection of the  
      ' Northwind database. 
      .Fields.Append .CreateField("FirstName", dbText) 
      .Fields.Append .CreateField("LastName", dbText) 
      .Fields.Append .CreateField("Phone", dbText) 
      .Fields.Append .CreateField("Notes", dbMemo) 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "before appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
      ' Append the new TableDef object to the Northwind  
      ' database. 
      dbsNorthwind.TableDefs.Append tdfNew 
 
      Debug.Print "Properties of new TableDef object " & _ 
         "after appending to collection:" 
 
      ' Enumerate Properties collection of new TableDef  
      ' object. 
      For Each prpLoop In .Properties 
         On Error Resume Next 
         If prpLoop <> "" Then Debug.Print "  " & _ 
           prpLoop.Name & " = " & prpLoop 
         On Error GoTo 0 
      Next prpLoop 
 
   End With 
 
   ' Delete new TableDef object since this is a  
   ' demonstration. 
   dbsNorthwind.TableDefs.Delete "Contacts" 
 
   dbsNorthwind.Close 
 
```



