---
title: OLE DB Provider for Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 22735ede3150b8735902fb94e5b774df41592dca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593454"
---
# <a name="ole-db-provider-for-internet-publishing"></a>OLE DB プロバイダー for Internet Publishing

**適用先**: Access 2013、Office 2013

ADO [Record](record-object-ado.md) オブジェクトと [Stream](stream-object-ado.md) オブジェクトは、Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) と一緒に使用して、Web フォルダーや Microsoft FrontPage が提供するファイルなどのリソースにアクセスおよび操作できます。 ADO を使用して、 **Record** 、 **Stream** 、または [Recordset](recordset-object-ado.md) のソースを URL に指定することができます。 その後、リソースをアップロード、ダウンロード、移動、コピー、および削除したり、リソースのプロパティを直接操作することができるようになります。

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

- [Connection](provider-property-ado.md) オブジェクトの [Provider](connection-object-ado.md) プロパティに Msdaipp.dso を指定します。次に例を示します。
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> *Provider* 接続文字列キーワードまたは **Provider** プロパティのいずれかでプロバイダーの値として明示的に Msdaipp.dso を指定すると、接続文字列に "URL=" を使用することはできません。 そのようにした場合は、エラーが発生します。 代わりに、このトピックの前に示した URL を指定します。

Internet Publishing Provider の詳細については、「[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)」を参照してください。または、OLE DB Provider for Internet Publishing が一緒にインストールされるソース アプリケーションである Windows 2000、Office 2000、または Internet Explorer 5.0 に付属しているプロバイダー マニュアルを参照してください。

