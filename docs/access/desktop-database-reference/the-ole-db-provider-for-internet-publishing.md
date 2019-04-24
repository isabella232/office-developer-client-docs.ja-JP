---
title: OLE DB Provider for Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 617dca5ced5410e2023657ea1b0b748066f7843f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314057"
---
# <a name="ole-db-provider-for-internet-publishing"></a><span data-ttu-id="40dce-102">OLE DB Provider for Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="40dce-102">OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="40dce-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="40dce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="40dce-104">ADO [Record](record-object-ado.md)オブジェクトと[Stream](stream-object-ado.md)オブジェクトは、microsoft OLE DB provider for internet publishing (internet publishing provider) と共に使用して、web フォルダーや microsoft FrontPage で提供されるファイルなどのリソースにアクセスしたり、操作したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="40dce-104">The ADO [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as web folders or files served by Microsoft FrontPage.</span></span> <span data-ttu-id="40dce-105">ADO を使用して、 **Record** 、 **Stream** 、または [Recordset](recordset-object-ado.md) のソースを URL に指定することができます。</span><span class="sxs-lookup"><span data-stu-id="40dce-105">With ADO, you can specify the source of a **Record**, **Stream**, or [Recordset](recordset-object-ado.md) to be a URL.</span></span> <span data-ttu-id="40dce-106">その後、リソースをアップロード、ダウンロード、移動、コピー、および削除したり、リソースのプロパティを直接操作することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="40dce-106">You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties.</span></span>

<span data-ttu-id="40dce-107">Internet Publishing Provider で **Records** と **Streams** を使用するコード例については、「 [インターネットに発行するためのシナリオ](internet-publishing-scenario.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="40dce-107">For example code using **Records** and **Streams** with the Internet Publishing Provider, see the [Internet Publishing Scenario](internet-publishing-scenario.md).</span></span>

<span data-ttu-id="40dce-p102">Internet Publishing Provider は、Microsoft Windows 2000 と共にインストールされます。Internet Publishing Provider の初期のバージョンは、Microsoft Office 2000 および Microsoft Internet Explorer 5.0 でも使用できます。</span><span class="sxs-lookup"><span data-stu-id="40dce-p102">The Internet Publishing Provider is installed with Microsoft Windows 2000. Earlier versions of the Internet Publishing Provider are also available with Microsoft Office 2000 and Microsoft Internet Explorer 5.0.</span></span>

<span data-ttu-id="40dce-110">ADO を Internet Publishing Provider に接続するには、3 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="40dce-110">There are three ways to connect ADO to the Internet Publishing Provider:</span></span>

- <span data-ttu-id="40dce-p103">接続文字列に "URL=" を指定します。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="40dce-p103">Specify "URL=" in the connection string. For example:</span></span>
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- <span data-ttu-id="40dce-113">接続文字列の *Provider* キーワードに Msdaipp.dso を指定します。</span><span class="sxs-lookup"><span data-stu-id="40dce-113">Specify Msdaipp.dso for the *Provider* keyword of the connection string.</span></span> <span data-ttu-id="40dce-114">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="40dce-114">For example:</span></span>
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- <span data-ttu-id="40dce-115">[Connection](provider-property-ado.md) オブジェクトの [Provider](connection-object-ado.md) プロパティに Msdaipp.dso を指定します。</span><span class="sxs-lookup"><span data-stu-id="40dce-115">Specify Msdaipp.dso for the [Provider](provider-property-ado.md) property of the [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="40dce-116">次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="40dce-116">For example:</span></span>
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> <span data-ttu-id="40dce-117">*Provider* 接続文字列キーワードまたは **Provider** プロパティのいずれかでプロバイダーの値として明示的に Msdaipp.dso を指定すると、接続文字列に "URL=" を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="40dce-117">If Msdaipp.dso is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="40dce-118">そのようにした場合は、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="40dce-118">If you do, an error will occur.</span></span> <span data-ttu-id="40dce-119">代わりに、このトピックで前述したように URL を指定するだけです。</span><span class="sxs-lookup"><span data-stu-id="40dce-119">Instead, simply specify the URL as shown earlier in this topic.</span></span>

<span data-ttu-id="40dce-120">Internet Publishing Provider の詳細については、「[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)」を参照してください。または、OLE DB Provider for Internet Publishing が一緒にインストールされるソース アプリケーションである Windows 2000、Office 2000、または Internet Explorer 5.0 に付属しているプロバイダー マニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="40dce-120">For more specific information about the Internet Publishing Provider, see [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), or the provider documentation provided with the source application with which the OLE DB Provider for Internet Publishing was installed: Windows 2000, Office 2000, or Internet Explorer 5.0.</span></span>

