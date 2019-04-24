---
title: レプリケーション API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329520"
---
# <a name="about-the-replication-api"></a>レプリケーション API について

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
レプリケーション API は、MAPI メッセージストアプロバイダーが、microsoft outlook 2013 または microsoft outlook 2010 アイテムを、そのプロバイダに対して作成されたサーバーとプライベート .pst ベースのローカルストアとの間で同期する機能を提供します。 
  
> [!NOTE]
> MAPI メッセージストアプロバイダーは、[レプリケーション状態マシンについて](about-the-replication-state-machine.md)の指示に従って、レプリケーション API を実装する必要があります。 プロバイダーは、他のプロバイダー用に作成された個人用ストアに対してのみ API を使用する必要があります。他のプロバイダー用に作成された個人用ストアでは、それぞれのサーバーに対して独自のレプリケーションメカニズムが既にセットアップされている場合があるためです。 たとえば、オフラインフォルダーファイル (.ost) は、Microsoft Exchange サーバーとの間でレプリケーション関係を維持します。 
  
レプリケーション API を使用するには、最初に**[nstserviceentry](nstserviceentry.md)** を呼び出すことによって、MAPI メッセージストアプロバイダーが .pst ベースのローカルストアを開いてラップする必要があります。 プロバイダーは、API の主なインターフェイスである**[iostx](iostxiunknown.md)** と**[ipstx](ipstxiunknown.md)** を使用して、レプリケーションを実行することができます。 **ipstx**は、IMsgStore に対するクエリによって提供され[ます。 imapiprop](imsgstoreimapiprop.md)、および**[GetSyncObject](ipstx-getsyncobject.md)** によって**iostx**が提供されます。 
  
## <a name="the-iostx-interface"></a>iostx インターフェイス

**iostx**インターフェイスは、レプリケーション API で同期を実行するプライマリインターフェイスです。 **iostx**ローカルストアを一連の状態で移動し、ローカルストアの変更に関する各状態の情報を取得します。また、サーバー上の変更をローカルストアに通知することもできます。 レプリケーション API でも、同期をサポートする多くのデータ構造が指定されています。 
  
この api のクライアントとしてのストアプロバイダーは、レプリケーション API を使用して、ローカルストアをラップし、これらの状態を使用して、ローカルストアに対する変更 (フォルダー階層への変更、新しいアイテムの追加など) をサーバーにプッシュします。また、サーバー上の変更に関する情報と、その情報を**iostx**インターフェイスに提供します。 **iostx**インターフェイスは、Microsoft Exchange Server によって提供される増分変更同期 (ICS) を採用します。 ics の詳細については、「 [ics の評価基準](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx)」を参照してください。 **iostx**を使用すると、クライアントは ICS を使用して、ローカルストア上の階層またはコンテンツに対する増分の変更を監視し、同期します。 
  
## <a name="the-ipstx-interface"></a>ipstx インターフェイス

 **** ipstx およびその他の5つの * * ipstx n * * **** ipstx *n* * * は、 **iostx**インターフェイスを介してレプリケーションを実行するときに使用できるヘルパー機能を提供します。 たとえば、 **[ipstx:: EmulateSpooler](ipstx-emulatespooler.md)** を使用すると、ローカルストアが Outlook プロトコルマネージャーをエミュレートして、送信メッセージをサーバーにスプールするようにすることができます。 
  
レプリケーション中の状態遷移の詳細については、「 [replication state Machine につい](about-the-replication-state-machine.md)て」を参照してください。
  
## <a name="the-replication-api"></a>レプリケーション API

レプリケーション API は、次の日、データ型、およびインターフェイスを提供します。 ラップされた個人用フォルダーファイル (PST) のストアプロバイダーのサンプルの実装については、「[サンプルのラップされた PST ストアプロバイダーについ](about-the-sample-wrapped-pst-store-provider.md)て」を参照してください。
  
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
    
- **[頻度](sync.md)**
    
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
  
- **[iostx](iostxiunknown.md)**
    
- **[ipstx](ipstxiunknown.md)**
    
- **[IPSTX2](ipstx2ipstx.md)**
    
- **[IPSTX3](ipstx3ipstx2.md)**
    
- **[IPSTX4](ipstx4ipstx3.md)**
    
- **[IPSTX5](ipstx5ipstx4.md)**
    
- **[IPSTX6](ipstx6ipstx5.md)**
    

