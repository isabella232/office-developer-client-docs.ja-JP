---
title: OLE DB Provider for Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7315df5a20cf032fc256f03893531f58857d470a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998666"
---
# <a name="ole-db-provider-for-internet-publishing"></a>OLE DB Provider for Internet Publishing

**適用されます**Access 2013、Office 2013。

ADO[レコード](record-object-ado.md)および[ストリーム](stream-object-ado.md)オブジェクトは、そのインターネット公開インターネット発行プロバイダー () にアクセスし、web フォルダーまたは FrontPage によって処理されるファイルなどのリソースを操作する Microsoft OLE DB プロバイダーを使用できます。 ADO を使用して、 **Record** 、 **Stream** 、または [Recordset](recordset-object-ado.md) のソースを URL に指定することができます。 その後、リソースをアップロード、ダウンロード、移動、コピー、および削除したり、リソースのプロパティを直接操作することができるようになります。

Internet Publishing Provider で **Records** と **Streams** を使用するコード例については、「 [インターネットに発行するためのシナリオ](internet-publishing-scenario.md)」を参照してください。

Internet Publishing Provider は、Microsoft Windows 2000 と共にインストールされます。Internet Publishing Provider の初期のバージョンは、Microsoft Office 2000 および Microsoft Internet Explorer 5.0 でも使用できます。

ADO を Internet Publishing Provider に接続するには、3 つの方法があります。

- 接続文字列に "URL=" を指定します。次に例を示します。
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- 接続文字列の*Provider*キーワードに Msdaipp.dso を指定します。 次に例を示します。
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- [Connection](provider-property-ado.md) オブジェクトの [Provider](connection-object-ado.md) プロパティに Msdaipp.dso を指定します。次に例を示します。
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> プロバイダー、*プロバイダー*の接続文字列キーワードまたは**プロバイダー**のプロパティのいずれかの値として Msdaipp.dso が明示的に指定されている場合は使用できません"URL ="接続文字列にします。 "URL=" を使用すると、エラーが発生します。 このトピックで前述したように、URL を単に指定代わりに、します。

Internet Publishing Provider の詳細については、「[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)」を参照してください。または、OLE DB Provider for Internet Publishing が一緒にインストールされるソース アプリケーションである Windows 2000、Office 2000、または Internet Explorer 5.0 に付属しているプロバイダー マニュアルを参照してください。

