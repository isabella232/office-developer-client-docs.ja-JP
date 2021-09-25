---
title: TNEF を使用した受信者テーブルのエンコード
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 4cce961a4b601f433adac1b11a650165ecf71835
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621144"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>TNEF を使用した受信者テーブルのエンコード

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ほとんどのメッセージング システムは受信者リストを直接サポートしていますので、TNEF ストリームへの受信者テーブルのエンコードはほとんど必要ありません。 一般に、受信者のプロパティはメッセージ ヘッダーで送信されます。 受信者テーブルを含める必要がある場合、TNEF は受信者テーブルを通常の処理の一部としてエンコードできます。 これは、TNEF 処理の初期フェーズ中に行われます。 トランスポート プロバイダーは、包含リストで指定された PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを使用して[ITnef::AddProps](itnef-addprops.md)メソッドを呼び出すことによって、メッセージの受信者テーブルを含めできます。  TNEF はメッセージから受信者テーブルを取得し、列セットを照会し、テーブルのすべての行を TNEF ストリームに処理します。
  
トランスポート プロバイダーがエンコードされる前に受信者テーブルを変更する必要がある場合は、別のメソッドを使用できます。 トランスポート プロバイダーは、必要なテーブルを作成し [、ITnef::EncodeRecips メソッドを呼び出](itnef-encoderecips.md) します。 _lpRecipTable_ パラメーターで NULL が渡された場合、受信者テーブルは **ITnef::AddProps** の説明に従ってメッセージから直接取得されます。
  

