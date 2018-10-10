---
title: '手順 2: Main リスト ボックスを初期化する'
TOCTitle: 'Step 2: Initialize the Main List Box'
ms:assetid: 81e4dcfd-6ee0-b5f9-9ea3-026c38c26bf0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249562(v=office.15)
ms:contentKeyID: 48545967
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f2b6b4d79262796aa8e9090d673a439a550f042c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478632"
---
# <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="559b5-102">手順 2: Main リスト ボックスを初期化する</span><span class="sxs-lookup"><span data-stu-id="559b5-102">Step 2: Initialize the Main List Box</span></span>


<span data-ttu-id="559b5-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="559b5-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="step-2-initialize-the-main-list-box"></a><span data-ttu-id="559b5-104">手順 2: Main リスト ボックスを初期化する</span><span class="sxs-lookup"><span data-stu-id="559b5-104">Step 2: Initialize the Main List Box</span></span>

<span data-ttu-id="559b5-105">**グローバルな Record オブジェクトと Recordset オブジェクトを宣言するには**</span><span class="sxs-lookup"><span data-stu-id="559b5-105">**To declare global Record and Recordset objects**</span></span>

  - <span data-ttu-id="559b5-106">Form1 の (General) (Declarations) に次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="559b5-106">Insert the following code into the (General) (Declarations) for Form1:</span></span>
    
    ```vb 
     
    Option Explicit 
    Dim grec As Record 
    Dim grs As Recordset 
    ```
    
    <span data-ttu-id="559b5-107">このコードによって、このシナリオで後ほど使用する **Record** オブジェクトと **Recordset** オブジェクトへのグローバル オブジェクト参照を宣言します。</span><span class="sxs-lookup"><span data-stu-id="559b5-107">This code declares global object references for **Record** and **Recordset** objects that will be used later in this scenario.</span></span>

<span data-ttu-id="559b5-108">**URL に接続して lstMain にデータを設定するには**</span><span class="sxs-lookup"><span data-stu-id="559b5-108">**To connect to a URL and populate lstMain**</span></span>

  - <span data-ttu-id="559b5-109">Form1 の Form Load イベント ハンドラーに次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="559b5-109">Insert the following code into the Form Load event handler for Form1:</span></span>
    
    ```vb 
     
    Private Sub Form_Load() 
        Set grec = New Record 
        Set grs = New Recordset 
        grec.Open "", "URL=https://servername/foldername/", , _ 
            adOpenIfExists Or adCreateCollection 
        Set grs = grec.GetChildren 
        While Not grs.EOF 
            lstMain.AddItem grs(0) 
            grs.MoveNext 
        Wend 
    End Sub 
    ```
    
    <span data-ttu-id="559b5-110">このコードによって、グローバルな **Record** オブジェクトと **Recordset** オブジェクトのインスタンスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="559b5-110">This code instantiates the global **Record** and **Recordset** objects.</span></span> <span data-ttu-id="559b5-111">**レコード**grec、 **ActiveConnection**として指定された URL を使用して開かれます。</span><span class="sxs-lookup"><span data-stu-id="559b5-111">The **Record**, grec, is opened with a URL specified as the **ActiveConnection**.</span></span> <span data-ttu-id="559b5-112">URL が存在する場合は開かれますが、存在しない場合は作成されます。</span><span class="sxs-lookup"><span data-stu-id="559b5-112">If the URL exists, it is opened; if it does not already exist, it is created.</span></span> <span data-ttu-id="559b5-113">"https://servername/foldername/" は、使用する環境での有効な URL に置き換える必要があります。</span><span class="sxs-lookup"><span data-stu-id="559b5-113">Note that you should replace "https://servername/foldername/" with a valid URL from your environment.</span></span> <span data-ttu-id="559b5-114">**レコード**grec の子の**レコード セット**grs が開かれます。</span><span class="sxs-lookup"><span data-stu-id="559b5-114">The **Recordset**, grs, is opened on the children of the **Record**, grec.</span></span> <span data-ttu-id="559b5-115">次に、URL に発行されたリソースのファイル名が lstMain に設定されます。</span><span class="sxs-lookup"><span data-stu-id="559b5-115">Then lstMain is populated with the file names of the resources published to the URL.</span></span>

