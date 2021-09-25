---
title: レプリケーション API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 1d0d67c9a766ebafec6d44e3e54986f50bf7b4d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592743"
---
# <a name="about-the-replication-api"></a>レプリケーション API について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
レプリケーション API は、MAPI メッセージ ストア プロバイダーがサーバーと、そのプロバイダー用に作成されたプライベートの .pst ベースのローカル ストアとの間で Microsoft Outlook 2013 または Microsoft Outlook 2010 アイテムを同期する機能を提供します。 
  
> [!NOTE]
> MAPI メッセージ ストア プロバイダーは、「レプリケーション ステート マシンについて」の手順に従ってレプリケーション API [を実装する必要があります](about-the-replication-state-machine.md)。 プロバイダーは、他のプロバイダー用に作成された個人用ストアが、既にそれぞれのサーバーで独自のレプリケーション メカニズムを設定している可能性があるため、他のプロバイダー用に作成された個人用ストアではなく、自身用に作成された個人用ストアでのみ API を使用する必要があります。 たとえば、オフライン フォルダー ファイル (.ost) は、Microsoft サーバーと独自のレプリケーションExchangeします。 
  
レプリケーション API を使用するには、MAPI メッセージ ストア プロバイダーが **[NSTServiceEntry](nstserviceentry.md)** を呼び出して .pst ベースのローカル ストアを開いてラップする必要があります。 プロバイダーは **[、API、IOSTX、IPSTX](iostxiunknown.md)** の主要なインターフェイス **[](ipstxiunknown.md)** を使用してレプリケーションを実行できます。 **IPSTX** は [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)でのクエリによって提供され **、IOSTX** は **[IPSTX::GetSyncObject によって提供されます](ipstx-getsyncobject.md)**。 
  
## <a name="the-iostx-interface"></a>IOSTX インターフェイス

**IOSTX インターフェイス** は、レプリケーション API で同期を実行するプライマリ インターフェイスです。 **IOSTX** は、一連の状態を通じてローカル ストアを移動し、ローカル ストアの変更に関する各状態の情報を取得し、サーバー上の変更をローカル ストアに通知します。 レプリケーション API では、同期をサポートする多くのデータ構造も指定します。 
  
ストア プロバイダーは、この API のクライアントとして、レプリケーション API を使用してローカル ストアをラップし、これらの状態を移動し、ローカル ストアでの変更 (フォルダー階層の変更や新しいアイテムの追加など) をサーバーにプッシュし、サーバー上の変更に関する情報を取得し、その情報を **IOSTX** インターフェイスに提供します。 **IOSTX インターフェイスは**、ユーザーが提供する増分変更同期 (ICS) をMicrosoft Exchange Server。 ICS の詳細については [、「ICS 評価基準」を参照してください](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)。 **IOSTX を介** して、クライアントは ICS を使用して、ローカル ストア上の階層またはコンテンツに対する増分変更を監視および同期します。 
  
## <a name="the-ipstx-interface"></a>IPSTX インターフェイス

 **IPSTX および** IPSTXから継承する他の 5 つの ****IPSTX** n ** インターフェイスは **、IOSTX** インターフェイスを介してレプリケーションを実行するときに使用できるヘルパー機能を提供します。 たとえば **[、IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** を使用すると、ローカル ストアで Outlook プロトコル マネージャーをエミュレートして、送信メッセージをサーバーにスプールできます。 
  
レプリケーション中の状態遷移の詳細については、「レプリケーションステート マシンについて [」を参照してください](about-the-replication-state-machine.md)。
  
## <a name="the-replication-api"></a>レプリケーション API

レプリケーション API には、次の定義、データ型、およびインターフェイスが含まれます。 ラップされた個人用フォルダー ファイル (PST) のストア プロバイダーの実装例については、「サンプル ラップされた PST ストア プロバイダーについて」 [を参照してください](about-the-sample-wrapped-pst-store-provider.md)。
  
定義:
  
- [レプリケーション API の定数](mapi-constants.md)
    
関数
  
- **[NSTServiceEntry](nstserviceentry.md)**
    
データ型:
  
- **[DNHIER](dnhier.md)**
    
- **[DNTBL](dntbl.md)**
    
- **[DNTBLE](dntble.md)**
    
- **[FEID](feid.md)**
    
- **[HDRSYNC](hdrsync.md)**
    
- **[LTID](ltid.md)**
    
- **[MEID](meid.md)**
    
- **[OLFI](olfi.md)**
    
- **[SKEY](skey.md)**
    
- **[SYNC](sync.md)**
    
- **[SYNCCONT](synccont.md)**
    
- **[SYNCSTATE](syncstate.md)**
    
- **[UPDEL](updel.md)**
    
- **[UPDELE](updele.md)**
    
- **[UPFLD](upfld.md)**
    
- **[UPHIER](uphier.md)**
    
- **[UPMOV](upmov.md)**
    
- **[UPMSG](upmsg.md)**
    
- **[UPREAD](upread.md)**
    
- **[UPREADE](upreade.md)**
    
- **[UPTBL](uptbl.md)**
    
- **[UPTBLE](uptble.md)**
    
インターフェイス
  
- **[IOSTX](iostxiunknown.md)**
    
- **[IPSTX](ipstxiunknown.md)**
    
- **[IPSTX2](ipstx2ipstx.md)**
    
- **[IPSTX3](ipstx3ipstx2.md)**
    
- **[IPSTX4](ipstx4ipstx3.md)**
    
- **[IPSTX5](ipstx5ipstx4.md)**
    
- **[IPSTX6](ipstx6ipstx5.md)**
    

