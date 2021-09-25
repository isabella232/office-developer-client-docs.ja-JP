---
title: PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 1cf5b314-39fa-996f-fd88-00380ffbc4de
description: メッセージのセカンダリ アカウントendstampを指定します。
ms.openlocfilehash: 4acc8639be3b09a2a12fc402c7fc5bc2463af4db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557114"
---
# <a name="pidtagnextsendacct"></a>PidTagNextSendAcct

メッセージのセカンダリ アカウント "send" スタンプを指定します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|識別子:  <br/> |0x0E29  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |Outlookアプリケーション  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、MAPI メッセージ オブジェクトに適用されます。 受信したメッセージの場合、セカンダリ アカウントの "送信" スタンプは、転送または返信をプライマリ アカウントで送信できない場合に、転送または返信を送信するアカウントを示します。 送信メッセージの場合、セカンダリ アカウント "send" スタンプは、メッセージをプライマリ アカウントと一緒に送信できない場合に、メッセージを送信するアカウントを決定します。 その値は [、PROP_ACCT_SEND_STAMP](prop_acct_send_stamp.md) が送信されるアカウントの [IOlkAccount](iolkaccount.md) インターフェイスからの値です。 
  
## <a name="see-also"></a>関連項目

- [定数 (アカウント管理 API)](constants-account-management-api.md)
- [MAPI のプロパティ](https://msdn.microsoft.com/library/3b980217-b65b-442b-8c18-b8b9f3ff487a%28Office.15%29.aspx) 
- [PidTagNextSendAcct 標準プロパティ](https://msdn.microsoft.com/library/b7429c2e-0d9d-4921-9f56-9ecad817f8cb%28Office.15%29.aspx)

