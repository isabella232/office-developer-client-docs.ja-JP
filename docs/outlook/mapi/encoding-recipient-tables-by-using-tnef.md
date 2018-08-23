---
title: TNEF を使用した受信者テーブルのエンコード
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: aa2120b5d64eece76f8882489de4388b04afa053
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591346"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a>TNEF を使用した受信者テーブルのエンコード

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
TNEF ストリームに、受信者テーブルのエンコーディングは、多くのメッセージング システムの受信者の一覧を直接サポートするために必要はほとんどありません。 一般に、受信者のプロパティは、メッセージのヘッダーで送信されます。 受信者テーブルを含めることが必要な場合は、TNEF は、通常の処理の一部として受信者テーブルをエンコードできます。 これは、は、TNEF の処理の初期段階で行われます。 トランスポート プロバイダーは、信頼のリストで指定されている**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) プロパティを使用して、 [ITnef::AddProps](itnef-addprops.md)メソッドを呼び出すことによって、メッセージの受信者テーブルを含めることができます。 TNEF は、メッセージの受信者テーブルを取得、列セットに対してクエリを実行し、TNEF ストリームに、テーブルのすべての行を処理します。
  
別の方法では、トランスポート プロバイダーをエンコードする前に、受信者テーブルを変更する必要がある場合があります。 トランスポート プロバイダーは、必要なテーブルを作成し、 [ITnef::EncodeRecips](itnef-encoderecips.md)メソッドを呼び出してできます。 _LpRecipTable_パラメーターに NULL を渡した場合、受信者テーブルから直接取得されますメッセージ**ITnef::AddProps**で説明されているようです。
  

