---
title: 読み取り、定期的なパターンの解析
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 75113097-b3ae-4d20-9796-85c62a592ef0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 694d63165bb820ffef1a29d1646861435fc4ed26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800247"
---
# <a name="read-and-parse-a-recurrence-pattern"></a><span data-ttu-id="457cd-103">読み取り、定期的なパターンの解析</span><span class="sxs-lookup"><span data-stu-id="457cd-103">Read and parse a recurrence pattern</span></span>
  
<span data-ttu-id="457cd-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="457cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="457cd-105">読み取り、予定の定期的なパターンを解析するのには、MAPI を使用できます。</span><span class="sxs-lookup"><span data-stu-id="457cd-105">MAPI can be used to read and parse a recurrence pattern for an appointment.</span></span>
  
<span data-ttu-id="457cd-106">ダウンロード、表示、および、このトピックで参照されている MFCMAPI アプリケーション プロジェクトからコードを実行する方法の詳細については、[このセクションで使用されるサンプルのインストール](how-to-install-the-samples-used-in-this-section.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="457cd-106">For information about how to download, view, and run the code from the MFCMAPI application project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-parse-a-recurrence-blob"></a><span data-ttu-id="457cd-107">パターン blob を解析するには</span><span class="sxs-lookup"><span data-stu-id="457cd-107">To parse a recurrence blob</span></span>

1. <span data-ttu-id="457cd-108">予定アイテムを開きます。</span><span class="sxs-lookup"><span data-stu-id="457cd-108">Open an appointment item.</span></span> <span data-ttu-id="457cd-109">メッセージを開く方法については、[メッセージを開く](opening-a-message.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="457cd-109">For information about opening a message, see [Opening a Message](opening-a-message.md).</span></span>
    
2. <span data-ttu-id="457cd-110">名前付きプロパティの**dispidApptRecur** ([PidLidAppointmentRecur の標準的なプロパティ](pidlidappointmentrecur-canonical-property.md)) を取得します。</span><span class="sxs-lookup"><span data-stu-id="457cd-110">Retrieve the named property **dispidApptRecur** ([PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md)).</span></span> <span data-ttu-id="457cd-111">名前付きプロパティを取得する方法の詳細については、 [MAPI 名前付きプロパティ](mapi-named-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="457cd-111">For information about retrieving named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span>
    
3. <span data-ttu-id="457cd-112">予定の定期的なパターンの構造を読み取るには、 [[MS OXOCAL]](http://msdn.microsoft.com/ja-jp/library/cc425490%28EXCHG.80%29.aspx)の指示に従います。</span><span class="sxs-lookup"><span data-stu-id="457cd-112">Follow the guidance in [[MS-OXOCAL]](http://msdn.microsoft.com/ja-jp/library/cc425490%28EXCHG.80%29.aspx) to read the appointment recurrence pattern structure.</span></span> 
    
<span data-ttu-id="457cd-113">MFCMAPI 参照アプリケーションの最後の手順を説明する、 `BinToAppointmentRecurrencePatternStruct` MFCMapi プロジェクトの InterpretProp2.cpp のソース ファイル内の関数です。</span><span class="sxs-lookup"><span data-stu-id="457cd-113">The MFCMAPI reference application demonstrates the last step with the  `BinToAppointmentRecurrencePatternStruct` function in the InterpretProp2.cpp source file of the MFCMapi project.</span></span> <span data-ttu-id="457cd-114">`BinToAppointmentRecurrencePatternStruct`関数のパラメーターとしてのメモリ内のバッファーにポインターを取得します。</span><span class="sxs-lookup"><span data-stu-id="457cd-114">The  `BinToAppointmentRecurrencePatternStruct` function takes a pointer to a buffer in memory as a parameter.</span></span> <span data-ttu-id="457cd-115">MFCMAPI アプリケーションは、最初に名前付きプロパティ、プロパティ タグに、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを使用してプロパティの値を要求することによって**dispidApptRecur**をマップすることによって、このバッファーを取得します。</span><span class="sxs-lookup"><span data-stu-id="457cd-115">The MFCMAPI application obtains this buffer by first mapping the **dispidApptRecur** named property to a property tag, then by requesting the property's value using the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="457cd-116">プロパティが**GetProps**メソッドを使用して取得するのには大きすぎる場合は、MFCMAPI は[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを使用してプロパティを取得するためにストリームのインタ フェースを開きます。</span><span class="sxs-lookup"><span data-stu-id="457cd-116">If the property is too large to retrieve using the **GetProps** method, MFCMAPI opens a stream interface to retrieve the property using the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="457cd-117">MFCMAPI アプリケーションは、バッファーを構築するのには、ストリームからデータを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="457cd-117">The MFCMAPI application then reads the data out of the stream to build the buffer.</span></span> 
  
<span data-ttu-id="457cd-118">バッファーの形式については、 [PidLidAppointmentRecur の標準的なプロパティ](pidlidappointmentrecur-canonical-property.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="457cd-118">For information about the format of the buffer, see the [PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md).</span></span> <span data-ttu-id="457cd-119">バッファー内のデータの大部分は、バイトを読み取る必要があります 1 つの固定数のフィールドで構成されます。</span><span class="sxs-lookup"><span data-stu-id="457cd-119">The bulk of the data in the buffer consists of fields of a fixed number of bytes, which must be read one after another.</span></span> <span data-ttu-id="457cd-120">いくつかのフィールドは、他のフィールドに特定の値が含まれているし、他のフィールドの値のいくつかのフィールドのサイズが異なる場合がある場合にのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="457cd-120">Some fields are present only if other fields contain certain values, and the size of some fields may depend on the value of other fields.</span></span> <span data-ttu-id="457cd-121">簿記の多くは、さまざまなフィールドを読み取るバッファーを解析します。</span><span class="sxs-lookup"><span data-stu-id="457cd-121">Parsing the buffer to read the various fields involves a lot of bookkeeping.</span></span> <span data-ttu-id="457cd-122">MFCMAPI という名前の内部ヘルパー クラスを使用して`CBinaryParser`この簿記をカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="457cd-122">MFCMAPI uses an internal helper class named  `CBinaryParser` to encapsulate this bookkeeping.</span></span> <span data-ttu-id="457cd-123">などの`CBinaryParser::GetDWORD`関数は、かどうか十分なバイト数、DWORD を読み取るバッファーに残っている値を読み取るし、ポインターを更新します。</span><span class="sxs-lookup"><span data-stu-id="457cd-123">For example, the  `CBinaryParser::GetDWORD` function checks whether enough bytes remain in the buffer to read a DWORD, and then reads the value and updates the pointers.</span></span> 
  
<span data-ttu-id="457cd-124">MFCMAPI アプリケーションを使用してバッファーは構造に解析された後、`AppointmentRecurrencePatternStructToString`構造体をユーザーに表示する文字列に変換する関数。</span><span class="sxs-lookup"><span data-stu-id="457cd-124">After the buffer has been parsed into a structure, the MFCMAPI application uses the  `AppointmentRecurrencePatternStructToString` function to convert the structure to a string to display to the user.</span></span> <span data-ttu-id="457cd-125">Outlook は、表示しますが、Outlook がそのロジックを構築するデータの raw データのビューではなく文字列と同じではありません。</span><span class="sxs-lookup"><span data-stu-id="457cd-125">This is not the same string Outlook would display, but is instead a raw view of the data upon which Outlook builds its logic.</span></span> 
  
<span data-ttu-id="457cd-126">データが破損しているか、定期的なパターンをエンコードするために必要なより多くのデータが含まれているバッファーが発生することができます。</span><span class="sxs-lookup"><span data-stu-id="457cd-126">It is possible to encounter a buffer which contains either corrupted data or more data than is needed to encode a recurrence pattern.</span></span> <span data-ttu-id="457cd-127">MFCMAPI アプリケーションはこれらのシナリオを特定するためには、データの量が正常に解析され、バッファーに残っているどのくらいのトラックを保持します。</span><span class="sxs-lookup"><span data-stu-id="457cd-127">To help identify those scenarios, the MFCMAPI application keeps track of how much data has been successfully parsed and how much remains in the buffer.</span></span> <span data-ttu-id="457cd-128">解析が完了した後、データがバッファーに残っている場合 MFCMAPI にはデータが含まれますこの"迷惑"構造内に調べることができますので。</span><span class="sxs-lookup"><span data-stu-id="457cd-128">If data remains in the buffer after parsing has completed, MFCMAPI includes this "junk data" in the structure so it can be examined.</span></span>
  
<span data-ttu-id="457cd-129">次の完全な一覧では、`BinToAppointmentRecurrencePatternStruct`関数です。</span><span class="sxs-lookup"><span data-stu-id="457cd-129">The following is the complete listing of the  `BinToAppointmentRecurrencePatternStruct` function.</span></span> 
  
```cpp
AppointmentRecurrencePatternStruct* BinToAppointmentRecurrencePatternStruct(ULONG cbBin, LPBYTE lpBin)
{
   if (!lpBin) return NULL;
   AppointmentRecurrencePatternStruct arpPattern = {0};
   CBinaryParser Parser(cbBin,lpBin);
   size_t cbBinRead = 0;
   arpPattern.RecurrencePattern = BinToRecurrencePatternStruct(cbBin,lpBin,&cbBinRead);
   Parser.Advance(cbBinRead);
   Parser.GetDWORD(&arpPattern.ReaderVersion2);
   Parser.GetDWORD(&arpPattern.WriterVersion2);
   Parser.GetDWORD(&arpPattern.StartTimeOffset);
   Parser.GetDWORD(&arpPattern.EndTimeOffset);
   Parser.GetWORD(&arpPattern.ExceptionCount);
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions)
   {
      arpPattern.ExceptionInfo = new ExceptionInfoStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExceptionInfo)
      {
         memset(arpPattern.ExceptionInfo,0,sizeof(ExceptionInfoStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].StartDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].EndDateTime);
            Parser.GetDWORD(&arpPattern.ExceptionInfo[i].OriginalStartDate);
            Parser.GetWORD(&arpPattern.ExceptionInfo[i].OverrideFlags);
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].SubjectLength2);
               if (arpPattern.ExceptionInfo[i].SubjectLength2 && arpPattern.ExceptionInfo[i].SubjectLength2 + 1 
                  == arpPattern.ExceptionInfo[i].SubjectLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].SubjectLength2,&arpPattern.ExceptionInfo[i].Subject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_MEETINGTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].MeetingType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDERDELTA)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderDelta);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_REMINDER)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].ReminderSet);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength);
               Parser.GetWORD(&arpPattern.ExceptionInfo[i].LocationLength2);
               if (arpPattern.ExceptionInfo[i].LocationLength2 && arpPattern.ExceptionInfo[i].LocationLength2 
                  + 1 == arpPattern.ExceptionInfo[i].LocationLength)
               {
                  Parser.GetStringA(arpPattern.ExceptionInfo[i].LocationLength2,&arpPattern.ExceptionInfo[i].Location);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_BUSYSTATUS)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].BusyStatus);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_ATTACHMENT)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].Attachment);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBTYPE)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].SubType);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_APPTCOLOR)
            {
               Parser.GetDWORD(&arpPattern.ExceptionInfo[i].AppointmentColor);
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock1Size);
   if (arpPattern.ReservedBlock1Size && arpPattern.ReservedBlock1Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock1Size,&arpPattern.ReservedBlock1);
   }
   if (arpPattern.ExceptionCount &&
      arpPattern.ExceptionCount == arpPattern.RecurrencePattern->ModifiedInstanceCount &&
      arpPattern.ExceptionCount < _MaxExceptions &&
      arpPattern.ExceptionInfo)
   {
      arpPattern.ExtendedException = new ExtendedExceptionStruct[arpPattern.ExceptionCount];
      if (arpPattern.ExtendedException)
      {
         memset(arpPattern.ExtendedException,0,sizeof(ExtendedExceptionStruct) * arpPattern.ExceptionCount);
         WORD i = 0;
         for (i = 0 ; i < arpPattern.ExceptionCount ; i++)
         {
            if (arpPattern.WriterVersion2 >= 0x0003009)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightValue);
               if (arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize > sizeof(DWORD))
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ChangeHighlight.ChangeHighlightSize 
                     - sizeof(DWORD),&arpPattern.ExtendedException[i].ChangeHighlight.Reserved);
               }
            }
            Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE1Size);
            if (arpPattern.ExtendedException[i].ReservedBlockEE1Size &&
                arpPattern.ExtendedException[i].ReservedBlockEE1Size < _MaxReservedBlock)
            {
               Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE1Size,&arpPattern.ExtendedException[i].ReservedBlockEE1);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].StartDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].EndDateTime);
               Parser.GetDWORD(&arpPattern.ExtendedException[i].OriginalStartDate);
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharSubjectLength);
               if (arpPattern.ExtendedException[i].WideCharSubjectLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharSubjectLength,&arpPattern.ExtendedException[i].WideCharSubject);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetWORD(&arpPattern.ExtendedException[i].WideCharLocationLength);
               if (arpPattern.ExtendedException[i].WideCharLocationLength)
               {
                  Parser.GetStringW(arpPattern.ExtendedException[i].WideCharLocationLength,&arpPattern.ExtendedException[i].WideCharLocation);
               }
            }
            if (arpPattern.ExceptionInfo[i].OverrideFlags & ARO_SUBJECT ||
               arpPattern.ExceptionInfo[i].OverrideFlags & ARO_LOCATION)
            {
               Parser.GetDWORD(&arpPattern.ExtendedException[i].ReservedBlockEE2Size);
               if (arpPattern.ExtendedException[i].ReservedBlockEE2Size && arpPattern.ExtendedException[i].ReservedBlockEE2Size < _MaxReservedBlock)
               {
                  Parser.GetBYTES(arpPattern.ExtendedException[i].ReservedBlockEE2Size,&arpPattern.ExtendedException[i].ReservedBlockEE2);
               }
            }
         }
      }
   }
   Parser.GetDWORD(&arpPattern.ReservedBlock2Size);
   if (arpPattern.ReservedBlock2Size && arpPattern.ReservedBlock2Size < _MaxReservedBlock)
   {
      Parser.GetBYTES(arpPattern.ReservedBlock2Size,&arpPattern.ReservedBlock2);
   }
   // Junk data remains.
   if (Parser.RemainingBytes() > 0)
   {
      arpPattern.JunkDataSize = Parser.RemainingBytes();
      Parser.GetBYTES(arpPattern.JunkDataSize,&arpPattern.JunkData);
   }
   AppointmentRecurrencePatternStruct* parpPattern = new AppointmentRecurrencePatternStruct;
   if (parpPattern)
   {
      *parpPattern = arpPattern;
   }
   return parpPattern;
}

```

## <a name="see-also"></a><span data-ttu-id="457cd-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="457cd-130">See also</span></span>

- [<span data-ttu-id="457cd-131">MAPI を使用して Outlook 2007 のアイテムを作成するには</span><span class="sxs-lookup"><span data-stu-id="457cd-131">Using MAPI to Create Outlook 2007 Items</span></span>](http://msdn.microsoft.com/ja-jp/library/cc678348%28office.12%29.aspx)

