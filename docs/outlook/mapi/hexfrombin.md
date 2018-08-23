---
title: HexFromBin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HexFromBin
api_type:
- COM
ms.assetid: 12b95657-1926-4a24-be63-40305ea6f990
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8f68de5e18d84c728241c188b932f99456f5be8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584836"
---
# <a name="hexfrombin"></a><span data-ttu-id="6db2f-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="6db2f-103">HexFromBin</span></span>

  
  
<span data-ttu-id="6db2f-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6db2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6db2f-105">2 進数を 16 進数の文字列形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="6db2f-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6db2f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="6db2f-106">Header file:</span></span>  <br/> |<span data-ttu-id="6db2f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="6db2f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6db2f-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="6db2f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6db2f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6db2f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6db2f-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="6db2f-110">Called by:</span></span>  <br/> |<span data-ttu-id="6db2f-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="6db2f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="6db2f-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6db2f-112">Parameters</span></span>

 <span data-ttu-id="6db2f-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="6db2f-113">_pb_</span></span>
  
> <span data-ttu-id="6db2f-114">[in]変換するバイナリ データへのポインター。</span><span class="sxs-lookup"><span data-stu-id="6db2f-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="6db2f-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="6db2f-115">_cb_</span></span>
  
> <span data-ttu-id="6db2f-116">[in]_Pb_パラメーターが指す、バイナリ データのバイト単位のサイズです。</span><span class="sxs-lookup"><span data-stu-id="6db2f-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="6db2f-117">_sz_</span><span class="sxs-lookup"><span data-stu-id="6db2f-117">_sz_</span></span>
  
> <span data-ttu-id="6db2f-118">[out]16 進数のバイナリ データを表す null で終わる ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="6db2f-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6db2f-119">Return value</span><span class="sxs-lookup"><span data-stu-id="6db2f-119">Return value</span></span>

<span data-ttu-id="6db2f-120">なし。</span><span class="sxs-lookup"><span data-stu-id="6db2f-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6db2f-121">注釈</span><span class="sxs-lookup"><span data-stu-id="6db2f-121">Remarks</span></span>

<span data-ttu-id="6db2f-122">**HexFromBin**関数は、バイナリ データのサイズが_cb_パラメーターで示される単位にポインターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="6db2f-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="6db2f-123">内_sz_文字列で返します (2 \* _cb_) + 1 バイトのメモリ、16 進数のバイナリ情報を表したものです。</span><span class="sxs-lookup"><span data-stu-id="6db2f-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="6db2f-124">バイトの値が 10 進数の 10 の場合は、たとえば、16 進数の文字列になります 0 a、文字列内の 2 つのバイトは 1 バイトに変換。</span><span class="sxs-lookup"><span data-stu-id="6db2f-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

