---
title: '手順 2: データを取得する'
TOCTitle: 'Step 2: Get the Data'
ms:assetid: e6be8801-6e57-d287-e8d2-348963706edc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250171(v=office.15)
ms:contentKeyID: 48548387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: eb206d003f0f5dc6714f00c54368e493856eed1f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872250"
---
# <a name="step-2-get-the-data"></a><span data-ttu-id="fdd88-102">手順 2: データを取得する</span><span class="sxs-lookup"><span data-stu-id="fdd88-102">Step 2: Get the Data</span></span>


<span data-ttu-id="fdd88-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fdd88-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="step-2-get-the-data"></a><span data-ttu-id="fdd88-104">手順 2: データの取得</span><span class="sxs-lookup"><span data-stu-id="fdd88-104">Step 2: Get the Data</span></span>

<span data-ttu-id="fdd88-p101">この手順では、ADO の **Recordset** を開いてクライアントに送信する準備を行うコードを記述します。Windows のメモ帳などのテキスト エディターで XMLResponse.asp ファイルを開き、次のコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="fdd88-p101">In this step, you will write the code to open an ADO **Recordset** and prepare to send it to the client. Open the file XMLResponse.asp with a text editor, such as Windows Notepad, and insert the following code:</span></span>

```vb 
 
<%@ language="VBScript" %> 
 
<!-- #include file='adovbs.inc' --> 
 
<% 
  Dim strSQL, strCon 
  Dim adoRec  
  Dim adoCon  
  Dim xmlDoc  
 
  ' You will need to change "slqServer" below to the name of the SQL  
  ' server machine to which you want to connect. 
  strCon = "Provider=sqloledb;Data Source=sqlServer;Initial Catalog=Pubs;Integrated Security=SSPI;" 
  Set adoCon = server.createObject("ADODB.Connection") 
  adoCon.Open strCon 
 
  strSQL = "SELECT Title, Price FROM Titles ORDER BY Price" 
  Set adoRec = Server.CreateObject("ADODB.Recordset") 
  adoRec.Open strSQL, adoCon, adOpenStatic, adLockOptimistic, adCmdText 
```

<span data-ttu-id="fdd88-107">StrCon のパラメーターのデータ ソースのパラメーターの値を Microsoft SQL Server コンピューターの名前に変更することを確認します。</span><span class="sxs-lookup"><span data-stu-id="fdd88-107">Be sure to change the value of the Data Source parameter in parameter in strCon to the name of your Microsoft SQL Server computer.</span></span>

<span data-ttu-id="fdd88-108">ファイルを開いたままで、次の手順に進みます。</span><span class="sxs-lookup"><span data-stu-id="fdd88-108">Keep the file open and go on to the next step.</span></span>

### <a name="next-step"></a><span data-ttu-id="fdd88-109">次のステップ</span><span class="sxs-lookup"><span data-stu-id="fdd88-109">Next step</span></span>

[<span data-ttu-id="fdd88-110">手順 3: データを送信する</span><span class="sxs-lookup"><span data-stu-id="fdd88-110">Step 3: Send the Data</span></span>](step-3-send-the-data.md)

