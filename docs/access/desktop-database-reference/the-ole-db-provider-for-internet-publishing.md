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
# <a name="ole-db-provider-for-internet-publishing"></a>OLE DB Provider for Internet Publishing

**適用先:** Access 2013、Office 2013

ADO [Record](record-object-ado.md)オブジェクトと[Stream](stream-object-ado.md)オブジェクトは、microsoft OLE DB provider for internet publishing (internet publishing provider) と共に使用して、web フォルダーや microsoft FrontPage で提供されるファイルなどのリソースにアクセスしたり、操作したりすることができます。 ADO を使用して、 **Record** 、 **Stream** 、または [Recordset](recordset-object-ado.md) のソースを URL に指定することができます。 その後、リソースをアップロード、ダウンロード、移動、コピー、および削除したり、リソースのプロパティを直接操作することができるようになります。

Internet Publishing Provider で **Records** と **Streams** を使用するコード例については、「 [インターネットに発行するためのシナリオ](internet-publishing-scenario.md)」を参照してください。

Internet Publishing Provider は、Microsoft Windows 2000 と共にインストールされます。Internet Publishing Provider の初期のバージョンは、Microsoft Office 2000 および Microsoft Internet Explorer 5.0 でも使用できます。

ADO を Internet Publishing Provider に接続するには、3 つの方法があります。

- 接続文字列に "URL=" を指定します。次に例を示します。
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- 接続文字列の *Provider* キーワードに Msdaipp.dso を指定します。 次に例を示します。
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- [Connection](provider-property-ado.md) オブジェクトの [Provider](connection-object-ado.md) プロパティに Msdaipp.dso を指定します。 次に例を示します。
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> *Provider* 接続文字列キーワードまたは **Provider** プロパティのいずれかでプロバイダーの値として明示的に Msdaipp.dso を指定すると、接続文字列に "URL=" を使用することはできません。 そのようにした場合は、エラーが発生します。 代わりに、このトピックで前述したように URL を指定するだけです。

Internet Publishing Provider の詳細については、「[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)」を参照してください。または、OLE DB Provider for Internet Publishing が一緒にインストールされるソース アプリケーションである Windows 2000、Office 2000、または Internet Explorer 5.0 に付属しているプロバイダー マニュアルを参照してください。

