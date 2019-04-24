---
title: OLFI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 44bfaadf-36f9-bd8e-6158-646533f6849e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 027905721b5730b4c3d78f496022b88a8e6b84d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279754"
---
# <a name="olfi"></a>OLFI

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用フォルダーファイル (PST) ストアプロバイダーが、新しいメッセージまたはフォルダーのエントリ ID をオフラインモードで割り当てるために使用する、長期 ID 構造のキュー。
  
## <a name="quick-info"></a>クイック ヒント

```cpp
typedef struct { 
    ULONG    ulVersion; 
    MAPIUID  muidReserved; 
    ULONG    ulReserved; 
    DWORD    dwAlloc; 
    DWORD    dwNextAlloc; 
    LTID     ltidAlloc; 
    LTID     ltidNextAlloc; 
} OLFI, *POLFI;
```

## <a name="members"></a>メンバー

 _ulversion_
  
- 構造のバージョン番号。 
    
 _muidreserved_
  
- このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。
    
 _ulreserved_
  
- このメンバーは、Outlook の内部使用のために予約されており、サポートされていません。
    
 _dwAlloc_
  
- 割り当てに使用できるエントリの数。 これらのエントリは、同じグローバル一意識別子 (GUID) を共有します。
    
 _dwnextalloc_
  
- 割り当ての次に使用可能なエントリの数。 これらのエントリは同じ GUID を共有します。
    
 _ltidAlloc_
  
- 現在割り当てられているエントリを識別する、長期的な ID 構造である**[ltid](ltid.md)**。 長期 ID 構造には、GUID と、ストア内のオブジェクトを識別するインデックスが含まれています。 また、GUID とインデックスは、オブジェクトの一意のエントリ ID を形成できます。 
    
 _ltidnextalloc_
  
- 次の利用可能なエントリを識別する長期 ID 構造。
    
## <a name="remarks"></a>解説

エントリ ID は、フォルダーまたはメッセージの4バイトの MAPI エントリ識別子です。 詳細については、「 [ENTRYID](https://msdn.microsoft.com/library/ms836424)」を参照してください。
  
PST ストアプロバイダーは、新しいオブジェクトにエントリ ID を割り当てるときに、最初にサーバーを識別する GUID と、ストア内のオブジェクトを識別するインデックスを必要とします。 guid はすべてのエントリ id で一意ではありませんが、guid とインデックスの組み合わせによって一意のエントリが提供されます。 この GUID とインデックスのペアは、 **olfi**構造の一部である、長い用語の ID 構造 ( **ltid**) によって追跡されます。 
  
PST ストアプロバイダーでは、GUID とインデックスのペアごとに**olfi**の**ltid**構造が物理的に保持されません。 現在使用可能な最初の GUID とインデックスのペアに対して、1つの**ltid**構造*ltidAlloc*を保持します。この同じ GUID を共有する使用可能なエントリの数 ( *dwAlloc* )。もう1つ**** は、別の guid を持つ、次の使用可能な guid とインデックスのペアの*ltidnextalloc*です。 PST ストアプロバイダーは、 **olfi**構造を使用して、それが渡された guid とインデックスを追跡します。仮想レベルでは、プロバイダーは、割り当ての準備が整っている多数の**ltid**構造の予約を保持します。  *dwAlloc*は、使用可能な**ltid**構造体のカウントを保持します。 
  
エントリ id の要求はブロックに入っています。 ブロックに対する要求がある場合、PST ストアプロバイダーは、要求されたサイズと*dwAlloc*を比較することによって、十分な予約があるかどうかを確認します。 十分な予約がある場合は、 *ltidAlloc*の GUID とインデックスを割り当て用に返します。 その後、要求されたサイズで*dwAlloc*を減らし、要求されたサイズで*ltidAlloc*のインデックスを増分します。 これにより、エントリ id の別のブロックに対する次の要求で、 *ltidAlloc*を割り当てるために PST ストアプロバイダーが準備されます。 GUID は次の要求に対して同じままであることに注意してください。 
  
要求のサイズが*dwAlloc*より大きい場合、PST ストアプロバイダーは、 *dwnextalloc*および*ltidnextalloc*で指定されている、次のものを予約で使用しようとします。 *dwnextalloc*と*ltidnalloc*をそれぞれ*dwAlloc*および*ltidAlloc*にコピーし、 *dwnextalloc*と*ltidnextalloc*を NULL に設定します。 
  
PST ストアプロバイダーをラップするプロバイダーは、 *ltidnextalloc*を定期的にチェックして、それが NULL であるかどうかを確認する必要があります。 その場合、プロバイダーはそれを新しい GUID で設定し、さらにエントリ id を割り当てることができるように、 *dwnextalloc*をリセットする必要があります。 
  
## <a name="see-also"></a>関連項目



[レプリケーション API について](about-the-replication-api.md)
  
[レプリケーション状態のマシンについて](about-the-replication-state-machine.md)
  
[LTID](ltid.md)

