---
title: メッセージの件名を作成します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70e18534-054f-49e7-9a5d-10db0db132d0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 419c9776b380436b1a7163803a8677fb6a89be97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799872"
---
# <a name="creating-a-message-subject"></a>メッセージの件名を作成します。

  
  
**適用されます**: Outlook 
  
**あるの PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))、メッセージの件名は、メッセージの目的を要約するために使用、省略可能なプロパティです。 設定する場合は、文字列を作成して文字 128 バイト以内です。 128 バイトの制限は、MAPI のによって課された制限ではありません。いくつかのメッセージ ストア プロバイダーによって課された制限することをお勧めします。 それを課すはプロバイダーとの相互運用性を確保するには、サブジェクトが 128 バイトに制限します。 
  
いくつかのメッセージ ストア プロバイダーは、 [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx)インターフェイスを使用して、ストリームに書き込むために**あるの PR_SUBJECT**を許可しないことに注意します。 
  
**されて**([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) は設定されていませんこのプロパティが応答でのみ設定され、メッセージを転送しました。 
  
