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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: a1bf02de914865e27c8c018aba8695c858888ae2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412577"
---
# <a name="hexfrombin"></a><span data-ttu-id="426c9-103">HexFromBin</span><span class="sxs-lookup"><span data-stu-id="426c9-103">HexFromBin</span></span>

  
  
<span data-ttu-id="426c9-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="426c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="426c9-105">バイナリ番号を16進数の文字列表現に変換します。</span><span class="sxs-lookup"><span data-stu-id="426c9-105">Converts a binary number into a string representation of a hexadecimal number.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="426c9-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="426c9-106">Header file:</span></span>  <br/> |<span data-ttu-id="426c9-107">Mapiutil</span><span class="sxs-lookup"><span data-stu-id="426c9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="426c9-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="426c9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="426c9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="426c9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="426c9-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="426c9-110">Called by:</span></span>  <br/> |<span data-ttu-id="426c9-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="426c9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void HexFromBin(
  LPBYTE pb,
  int cb,
  LPSTR sz
);
```

## <a name="parameters"></a><span data-ttu-id="426c9-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="426c9-112">Parameters</span></span>

 <span data-ttu-id="426c9-113">_pb_</span><span class="sxs-lookup"><span data-stu-id="426c9-113">_pb_</span></span>
  
> <span data-ttu-id="426c9-114">順番変換するバイナリデータへのポインター。</span><span class="sxs-lookup"><span data-stu-id="426c9-114">[in] Pointer to the binary data to be converted.</span></span> 
    
 <span data-ttu-id="426c9-115">_cb_</span><span class="sxs-lookup"><span data-stu-id="426c9-115">_cb_</span></span>
  
> <span data-ttu-id="426c9-116">順番_pb_パラメーターが指すバイナリデータのサイズ (バイト数)。</span><span class="sxs-lookup"><span data-stu-id="426c9-116">[in] Size, in bytes, of the binary data pointed to by the  _pb_ parameter.</span></span> 
    
 <span data-ttu-id="426c9-117">_sz_</span><span class="sxs-lookup"><span data-stu-id="426c9-117">_sz_</span></span>
  
> <span data-ttu-id="426c9-118">読み上げバイナリデータを16進数で表す null で終わる ASCII 文字列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="426c9-118">[out] Pointer to a null-terminated ASCII string representing the binary data in hexadecimal digits.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="426c9-119">Return value</span><span class="sxs-lookup"><span data-stu-id="426c9-119">Return value</span></span>

<span data-ttu-id="426c9-120">なし。</span><span class="sxs-lookup"><span data-stu-id="426c9-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="426c9-121">注釈</span><span class="sxs-lookup"><span data-stu-id="426c9-121">Remarks</span></span>

<span data-ttu-id="426c9-122">**HexFromBin**関数は、 _cb_パラメーターで指定されたサイズを持つバイナリデータの単位へのポインターを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="426c9-122">The **HexFromBin** function takes a pointer to a unit of binary data whose size is indicated by the  _cb_ parameter.</span></span> <span data-ttu-id="426c9-123">これは、(2 \* _cb_) + 1 バイトのメモリ内で、このバイナリ情報を16進数で表した_sz_文字列で返されます。</span><span class="sxs-lookup"><span data-stu-id="426c9-123">It returns in the  _sz_ string, within (2\*  _cb_)+1 bytes of memory, a representation of this binary information in hexadecimal numbers.</span></span> <span data-ttu-id="426c9-124">たとえば、バイト値が10進数の10の場合、16進文字列は0a になり、1バイトが文字列の2バイトに変換されます。</span><span class="sxs-lookup"><span data-stu-id="426c9-124">If the byte value is decimal 10, for example, the hexadecimal string will be 0A, so one byte converts to two bytes in the string.</span></span> 
  

