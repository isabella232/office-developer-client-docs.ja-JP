---
title: 通知の取り消し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8cd96dd22daeb98646a62672bd17f7de4d2f7dab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799756"
---
# <a name="canceling-a-notification"></a>通知の取り消し

  
  
**適用対象**: Outlook 
  
通知をキャンセルするには、クライアントは、アドバイス、ソースの**Unadvise**メソッドを呼び出します。 アドバイズ シンクへの参照を解放するのにはサービス ・ プロバイダーが発生するため、 **Unadvise**を呼び出すことが重要です。 サービス プロバイダーは、アドバイズ シンクへの参照を管理している限り、アドバイズ シンクは、 [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)呼び出しの受信を続行できます。 実際には、非同期であるのため、イベントの通知、クライアントが通知成功**Unadvise**の呼び出し後にも。 クライアントは、いつでも通知の受信を処理できる必要があります。 
  
サービス プロバイダーの実装が異なるため、通知をキャンセルするのには**Unadvise**の呼び出しに失敗したクライアント何も想定できませんに関するプロバイダーは、アドバイズ シンクへの参照を解放するとき。 サービス プロバイダーによっては、アドバイズ ソース バッファーが解放されるときにアドバイズ シンクへの参照をリリースします。 一部のサービス プロバイダーは必要ありません。 サービス プロバイダーは、アドバイズ シンクへの参照を管理している限り、そのアドバイズ シンクが通知を受信する続行できます。 
  

