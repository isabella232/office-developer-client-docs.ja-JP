---
title: メッセージ件名の作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332964"
---
# <a name="creating-a-message-subject"></a>メッセージ件名の作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの件名である PR_SUBJECT **(** [PidTagSubject)](pidtagsubject-canonical-property.md)は、メッセージの意図を要約するために使用されるオプションのプロパティです。 設定する場合は、文字列を 128 バイト以下にしてください。 128 バイトの制限は、MAPI によって課される制限ではありません。これは、一部のメッセージ ストア プロバイダーによって課される制限です。 これを行うプロバイダーとの相互運用性を確保するには、サブジェクトを 128 バイトに制限します。 
  
一部のメッセージ ストア プロバイダーでは、IStream インターフェイスPR_SUBJECTストリームへの書き込みが許可されていない[場合](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)があります。  
  
[設定しない **] PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md));このプロパティは、返信と転送されたメッセージにのみ設定されます。 
  

