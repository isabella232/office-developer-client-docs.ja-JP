---
title: メッセージの件名の作成
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 753834ba4df6d0239a484af380e4fe0aa45666b4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395687"
---
# <a name="creating-a-message-subject"></a>メッセージの件名の作成

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))、メッセージの件名は、メッセージの目的を要約するために使用、省略可能なプロパティです。 設定する場合は、文字列を作成して文字 128 バイト以内です。 128 バイトの制限は、MAPI のによって課された制限ではありません。いくつかのメッセージ ストア プロバイダーによって課された制限することをお勧めします。 それを課すはプロバイダーとの相互運用性を確保するには、サブジェクトが 128 バイトに制限します。 
  
いくつかのメッセージ ストア プロバイダーは、 [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)インターフェイスを使用して、ストリームに書き込むために**あるの PR_SUBJECT**を許可しないことに注意します。 
  
**されて**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) は設定されていませんこのプロパティが応答でのみ設定され、メッセージを転送しました。 
  

