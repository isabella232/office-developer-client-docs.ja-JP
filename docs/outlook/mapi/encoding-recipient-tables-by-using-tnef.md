---
title: TNEF を使用した受信者テーブルのエンコード
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417960"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>TNEF を使用した受信者テーブルのエンコード

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
ほとんどのメッセージング システムは受信者リストを直接サポートしていますので、TNEF ストリームへの受信者テーブルのエンコードはほとんど必要ありません。 一般に、受信者のプロパティはメッセージ ヘッダーで送信されます。 受信者テーブルを含める必要がある場合、TNEF は受信者テーブルを通常の処理の一部としてエンコードできます。 これは、TNEF 処理の初期フェーズ中に行われます。 トランスポート プロバイダーは、包含リストで指定された PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを使用して[ITnef::AddProps](itnef-addprops.md)メソッドを呼び出すことによって、メッセージの受信者テーブルを含めできます。  TNEF はメッセージから受信者テーブルを取得し、列セットを照会し、テーブルのすべての行を TNEF ストリームに処理します。
  
トランスポート プロバイダーがエンコードされる前に受信者テーブルを変更する必要がある場合は、別のメソッドを使用できます。 トランスポート プロバイダーは、必要なテーブルを作成し [、ITnef::EncodeRecips メソッドを呼び出](itnef-encoderecips.md) します。 _lpRecipTable_ パラメーターで NULL が渡された場合、受信者テーブルは **ITnef::AddProps** の説明に従ってメッセージから直接取得されます。
  

