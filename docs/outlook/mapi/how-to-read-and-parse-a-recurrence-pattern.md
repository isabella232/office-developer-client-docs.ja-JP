---
title: 定期的なアイテムのパターンを読み取って解析する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 75113097-b3ae-4d20-9796-85c62a592ef0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c226fe79fd002cda3c557fc8416c25f98ad33626
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345928"
---
# <a name="read-and-parse-a-recurrence-pattern"></a><span data-ttu-id="86b54-103">定期的なアイテムのパターンを読み取って解析する</span><span class="sxs-lookup"><span data-stu-id="86b54-103">Read and parse a recurrence pattern</span></span>
  
<span data-ttu-id="86b54-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="86b54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="86b54-105">MAPI を使用して、予定の定期的なパターンを読み取り、解析できます。</span><span class="sxs-lookup"><span data-stu-id="86b54-105">MAPI can be used to read and parse a recurrence pattern for an appointment.</span></span>
  
<span data-ttu-id="86b54-106">このトピックで参照されている MFCMAPI アプリケーション プロジェクトからコードをダウンロード、表示、実行する方法については、「このセクションで使用されるサンプルのインストール」 [を参照してください](how-to-install-the-samples-used-in-this-section.md)。</span><span class="sxs-lookup"><span data-stu-id="86b54-106">For information about how to download, view, and run the code from the MFCMAPI application project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-parse-a-recurrence-blob"></a><span data-ttu-id="86b54-107">定期的な BLOB を解析するには</span><span class="sxs-lookup"><span data-stu-id="86b54-107">To parse a recurrence blob</span></span>

1. <span data-ttu-id="86b54-108">予定アイテムを開きます。</span><span class="sxs-lookup"><span data-stu-id="86b54-108">Open an appointment item.</span></span> <span data-ttu-id="86b54-109">メッセージを開く方法については、「メッセージを開 [く」を参照してください](opening-a-message.md)。</span><span class="sxs-lookup"><span data-stu-id="86b54-109">For information about opening a message, see [Opening a Message](opening-a-message.md).</span></span>
    
2. <span data-ttu-id="86b54-110">名前付きプロパティ **dispidApptRecur** ([PidLidAppointmentRecur 標準プロパティ) を取得します](pidlidappointmentrecur-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="86b54-110">Retrieve the named property **dispidApptRecur** ([PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md)).</span></span> <span data-ttu-id="86b54-111">名前付きプロパティの取得の詳細については、「MAPI 名前付きプロパティ [」を参照してください](mapi-named-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="86b54-111">For information about retrieving named properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span>
    
3. <span data-ttu-id="86b54-112">[[MS-OXOCAL] のガイダンスに従って](https://msdn.microsoft.com/library/cc425490%28EXCHG.80%29.aspx)、予定の定期的なパターン構造を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="86b54-112">Follow the guidance in [[MS-OXOCAL]](https://msdn.microsoft.com/library/cc425490%28EXCHG.80%29.aspx) to read the appointment recurrence pattern structure.</span></span> 
    
<span data-ttu-id="86b54-113">MFCMAPI 参照アプリケーションは、MFCMapi プロジェクトの InterpretProp2.cpp ソース ファイル内の関数の最後の手順  `BinToAppointmentRecurrencePatternStruct` を示します。</span><span class="sxs-lookup"><span data-stu-id="86b54-113">The MFCMAPI reference application demonstrates the last step with the  `BinToAppointmentRecurrencePatternStruct` function in the InterpretProp2.cpp source file of the MFCMapi project.</span></span> <span data-ttu-id="86b54-114">この  `BinToAppointmentRecurrencePatternStruct` 関数は、メモリ内のバッファーへのポインターをパラメーターとして受け取ります。</span><span class="sxs-lookup"><span data-stu-id="86b54-114">The  `BinToAppointmentRecurrencePatternStruct` function takes a pointer to a buffer in memory as a parameter.</span></span> <span data-ttu-id="86b54-115">MFCMAPI アプリケーションは、最初に **dispidApptRecur** 名前付きプロパティをプロパティ タグにマッピングし、次に [IMAPIProp::GetProps](imapiprop-getprops.md) メソッドを使用してプロパティの値を要求することで、このバッファーを取得します。</span><span class="sxs-lookup"><span data-stu-id="86b54-115">The MFCMAPI application obtains this buffer by first mapping the **dispidApptRecur** named property to a property tag, then by requesting the property's value using the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="86b54-116">**GetProps** メソッドを使用してプロパティを取得するには大きすぎる場合、MFCMAPI はストリーム インターフェイスを開き [、IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを使用してプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="86b54-116">If the property is too large to retrieve using the **GetProps** method, MFCMAPI opens a stream interface to retrieve the property using the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="86b54-117">その後、MFCMAPI アプリケーションはストリームからデータを読み取り、バッファーを構築します。</span><span class="sxs-lookup"><span data-stu-id="86b54-117">The MFCMAPI application then reads the data out of the stream to build the buffer.</span></span> 
  
<span data-ttu-id="86b54-118">バッファーの形式については [、「PidLidAppointmentRecur 標準プロパティ」を参照してください](pidlidappointmentrecur-canonical-property.md)。</span><span class="sxs-lookup"><span data-stu-id="86b54-118">For information about the format of the buffer, see the [PidLidAppointmentRecur Canonical Property](pidlidappointmentrecur-canonical-property.md).</span></span> <span data-ttu-id="86b54-119">バッファー内のデータの大部分は、固定バイト数のフィールドで構成され、続々と読み取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="86b54-119">The bulk of the data in the buffer consists of fields of a fixed number of bytes, which must be read one after another.</span></span> <span data-ttu-id="86b54-120">一部のフィールドは、他のフィールドに特定の値が含まれている場合にのみ存在し、一部のフィールドのサイズは他のフィールドの値に依存する場合があります。</span><span class="sxs-lookup"><span data-stu-id="86b54-120">Some fields are present only if other fields contain certain values, and the size of some fields may depend on the value of other fields.</span></span> <span data-ttu-id="86b54-121">バッファーを解析してさまざまなフィールドを読み取るには、多くの簿記が必要です。</span><span class="sxs-lookup"><span data-stu-id="86b54-121">Parsing the buffer to read the various fields involves a lot of bookkeeping.</span></span> <span data-ttu-id="86b54-122">MFCMAPI は、このブックキーピングをカプセル化  `CBinaryParser` するために、という名前の内部ヘルパー クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="86b54-122">MFCMAPI uses an internal helper class named  `CBinaryParser` to encapsulate this bookkeeping.</span></span> <span data-ttu-id="86b54-123">たとえば、関数は、DWORD を読み取るのに十分なバイトがバッファー内に残っているかどうかをチェックし、値を読み取り、ポインター  `CBinaryParser::GetDWORD` を更新します。</span><span class="sxs-lookup"><span data-stu-id="86b54-123">For example, the  `CBinaryParser::GetDWORD` function checks whether enough bytes remain in the buffer to read a DWORD, and then reads the value and updates the pointers.</span></span> 
  
<span data-ttu-id="86b54-124">バッファーが構造体に解析された後、MFCMAPI アプリケーションは関数を使用して、構造体を文字列に変換してユーザー  `AppointmentRecurrencePatternStructToString` に表示します。</span><span class="sxs-lookup"><span data-stu-id="86b54-124">After the buffer has been parsed into a structure, the MFCMAPI application uses the  `AppointmentRecurrencePatternStructToString` function to convert the structure to a string to display to the user.</span></span> <span data-ttu-id="86b54-125">これは、表示される文字列と同Outlookではなく、ロジックを構築するデータの生Outlookです。</span><span class="sxs-lookup"><span data-stu-id="86b54-125">This is not the same string Outlook would display, but is instead a raw view of the data upon which Outlook builds its logic.</span></span> 
  
<span data-ttu-id="86b54-126">定期的なパターンをエンコードするために必要なデータよりも、破損したデータまたはより多くのデータを含むバッファーが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="86b54-126">It is possible to encounter a buffer which contains either corrupted data or more data than is needed to encode a recurrence pattern.</span></span> <span data-ttu-id="86b54-127">これらのシナリオを特定するために、MFCMAPI アプリケーションは、正常に解析されたデータの量とバッファー内の残りの量を追跡します。</span><span class="sxs-lookup"><span data-stu-id="86b54-127">To help identify those scenarios, the MFCMAPI application keeps track of how much data has been successfully parsed and how much remains in the buffer.</span></span> <span data-ttu-id="86b54-128">解析が完了した後にデータがバッファー内に残っている場合、MFCMAPI にはこの "迷惑データ" が構造に含まれるので、確認できます。</span><span class="sxs-lookup"><span data-stu-id="86b54-128">If data remains in the buffer after parsing has completed, MFCMAPI includes this "junk data" in the structure so it can be examined.</span></span>
  
<span data-ttu-id="86b54-129">関数の完全な一覧を次に示  `BinToAppointmentRecurrencePatternStruct` します。</span><span class="sxs-lookup"><span data-stu-id="86b54-129">The following is the complete listing of the  `BinToAppointmentRecurrencePatternStruct` function.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="86b54-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="86b54-130">See also</span></span>

- [<span data-ttu-id="86b54-131">MAPI を使用して 2007 Outlookアイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="86b54-131">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

