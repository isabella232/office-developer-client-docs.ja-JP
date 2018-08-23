---
title: レプリケーション API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 50b36ee60d00e06a1f5baa8726b5f27c4a3e6ce7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799597"
---
# <a name="about-the-replication-api"></a>レプリケーション API について

  
  
**適用対象**: Outlook 
  
レプリケーション API は、サーバーとプライベート .pst ベース ローカル ストア プロバイダーの作成は、Microsoft Outlook 2013 または Microsoft Outlook 2010 の項目を同期するには、MAPI メッセージ ストア プロバイダーの機能を提供します。 
  
> [!NOTE]
> MAPI メッセージ ストア プロバイダーは、[レプリケーションの状態マシンについて](about-the-replication-state-machine.md)の手順に従ってレプリケーション API を実装する必要があります。 プロバイダーは自体には、用に作成された個人用のストアにのみ、API を使用する必要があり、他のプロバイダー用に作成された個人用ストアではなくの個人ストアを作成するため他のプロバイダーが既に設定されているそれぞれのサーバーとのレプリケーション メカニズムを独自します。 たとえば、オフライン フォルダー ファイル (.ost) は、Microsoft Exchange サーバーとそのレプリケーション ・ リレーションシップを維持します。 
  
レプリケーション API を使用するには、MAPI メッセージ ストア プロバイダーする必要があります最初を開き**[NSTServiceEntry](nstserviceentry.md)** を呼び出すことによって .pst ベースのローカル ストアをラップします。 プロバイダーは、レプリケーションを実行するための API、 **[IOSTX](iostxiunknown.md)** **[IPSTX](ipstxiunknown.md)**、主要なインタ フェースを使用できます。 照会することで**IPSTX**が用意されている[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)、 **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**、 **IOSTX**が用意されているとします。 
  
## <a name="the-iostx-interface"></a>IOSTX インタ フェース

**IOSTX**インターフェイスは、レプリケーション API で同期を実行するプライマリ インターフェイスです。 **IOSTX**は、変更をサーバー上のローカル ストアに通知するとともに各状態で、ローカル ストア内の変更に関する情報を取得する一連の状態のローカル ストアを移動します。 レプリケーション API では、同期をサポートする多くのデータ構造体も指定します。 
  
ストア プロバイダーでは、この API では、クライアントとして API を使用して、レプリケーション、ローカル ストアをラップし、サーバーに (フォルダー階層、または新しい項目の追加に変更) などのローカル ストアに変更をプッシュし、取得するもこれらの状態間を移動します。**IOSTX**インターフェイスには、その情報を提供するサーバー上の変更に関する情報です。 **IOSTX**インターフェイスでは、増分変更の同期 (ICS) の Microsoft Exchange Server によって提供されるを適用します。 ICS の詳細については、 [ICS の評価基準](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx)を参照してください。 **IOSTX**クライアントを使用して ICS を監視し、階層、またはローカル ストア上のコンテンツへの増分変更を同期します。 
  
## <a name="the-ipstx-interface"></a>IPSTX インタ フェース

 **IPSTX**およびその他の 5 * * IPSTX *n* * * **IPSTX**から継承しているインターフェイスは、 **IOSTX**インターフェイスを使用するレプリケーションを実行するときに使用できるヘルパー機能を提供します。 たとえば、 **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** を使用すると、サーバーに送信するメッセージをスプールする Outlook プロトコル マネージャーをエミュレートするローカル ストアを作成できます。 
  
レプリケーション中に状態遷移の詳細については、[レプリケーションの状態マシンの詳細](about-the-replication-state-machine.md)を参照してください。
  
## <a name="the-replication-api"></a>レプリケーション API

レプリケーション API は、次の定義、データ型、およびインターフェイスを提供します。 ラップされた個人用フォルダー ファイル (PST) のストア プロバイダーの実装のサンプル、[についてはサンプル ラップ PST ストア プロバイダー](about-the-sample-wrapped-pst-store-provider.md)を参照してください。
  
定義
  
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
    
- **[同期状態](syncstate.md)**
    
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
    

