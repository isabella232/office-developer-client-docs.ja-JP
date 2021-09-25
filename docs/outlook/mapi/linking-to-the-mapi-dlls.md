---
title: MAPI DLL へのリンク
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 19fd4678-21d3-47a6-a439-1d4959cac407
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 10fa531c8ef11fb14a344957928b20728d39eba7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584179"
---
# <a name="linking-to-the-mapi-dlls"></a>MAPI DLL へのリンク

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI クライアントは **、LoadLibrary** 関数と **GetProcAddress** 関数を使用して、暗黙的に、または明示的Windows MAPI DLL にリンクできます。 MAPI DLL を明示的にリンクする方法については、「MAPI 関数への [リンク」を参照してください](how-to-link-to-mapi-functions.md)。
  
MAPI は、MAPIX に型定義ステートメントを提供します。次の各関数の H ヘッダー ファイル。
  
[MAPILogonEx](mapilogonex.md)
  
[MAPIUninitialize](mapiuninitialize.md)
  
[MAPIInitialize](mapiinitialize.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAdminProfiles](mapiadminprofiles.md)
  
MAPI DLL に明示的にリンクする場合は、これらの型定義を使用して、対応するエントリ ポイントを正しく呼び出します。
  
サービス プロバイダーは、MAPI 以外の機能 (MAPI とは完全に関連しない機能) を DLL に含めできます。 これらの機能を使用する必要がある場合は **、DLL** と FreeLibrary を使用する前に **LoadLibrary** を呼び出して、使用後に DLL をメモリから削除します。 MAPI はサービス プロバイダー DLL の MAPI 以外の使用を知らないため、必要なときに DLL を使用できる保証はありません。 MAPI は、サービスを必要とするアクティブ なセッションを持つクライアントが存在しなくなった場合に、サービス プロバイダー DLL を解放します。 
  

