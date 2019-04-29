---
title: MAPI DLL へのリンク
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 394537a60f4cb9603024115ccea67570291d8ac6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419304"
---
# <a name="linking-to-the-mapi-dlls"></a>MAPI DLL へのリンク

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
mapi クライアントは、暗黙的に、または Windows 関数**LoadLibrary**と**GetProcAddress**を使用して明示的に mapi dll にリンクできます。 mapi dll を明示的にリンクする方法については、「 [mapi 関数へのリンク](how-to-link-to-mapi-functions.md)」を参照してください。
  
MAPI では、mapix に type definition ステートメントが用意されています。H ヘッダーファイルを次の各関数に対して使用します。
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
これらの型定義を使用して、MAPI dll に明示的にリンクされている場合に、対応するエントリポイントを正しく呼び出します。
  
サービスプロバイダーには、DLL で mapi 以外の機能 (mapi に完全に関連しない機能) を含めることができます。 これらの機能を使用する必要がある場合は、dll と**FreeLibrary**を使用する前に**LoadLibrary**を呼び出して、使用した dll をメモリから削除します。 mapi は、サービスプロバイダー dll の非 mapi の使用を認識していないため、必要な場合に DLL が利用できるという保証はありません。 MAPI は、サービスを必要とするアクティブなセッションを持つクライアントがなくなったときに、サービスプロバイダー DLL を解放します。 
  

