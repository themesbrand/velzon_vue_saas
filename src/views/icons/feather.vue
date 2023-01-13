<script>
import { ActivityIcon, AirplayIcon, AlertCircleIcon, AlertOctagonIcon, AlertTriangleIcon, AlignCenterIcon, AlignJustifyIcon, AlignLeftIcon, AlignRightIcon, AnchorIcon, ApertureIcon, ArchiveIcon, ArrowDownCircleIcon, ArrowDownLeftIcon, ArrowDownRightIcon, ArrowDownIcon, ArrowLeftCircleIcon, ArrowLeftIcon, ArrowRightCircleIcon, ArrowRightIcon, ArrowUpCircleIcon, ArrowUpLeftIcon, ArrowUpRightIcon, ArrowUpIcon, AtSignIcon, AwardIcon, BarChart2Icon, BarChartIcon, BatteryChargingIcon, BatteryIcon, BellOffIcon, BellIcon, BluetoothIcon, BoldIcon, BookOpenIcon, BookIcon, BookmarkIcon, BoxIcon, BriefcaseIcon, CalendarIcon, CameraOffIcon, CameraIcon, CastIcon, CheckCircleIcon, CheckSquareIcon, CheckIcon, ChevronDownIcon, ChevronLeftIcon, ChevronRightIcon, ChevronUpIcon, ChevronsDownIcon, ChevronsLeftIcon, ChevronsRightIcon, ChevronsUpIcon, ChromeIcon, CircleIcon, ClipboardIcon, ClockIcon, CloudDrizzleIcon, CloudLightningIcon, CloudOffIcon, CloudRainIcon, CloudSnowIcon, CloudIcon, CodeIcon, CodepenIcon, CodesandboxIcon, CoffeeIcon, ColumnsIcon, CommandIcon, CompassIcon, CopyIcon, CornerDownLeftIcon, CornerDownRightIcon, CornerLeftDownIcon, CornerLeftUpIcon, CornerRightDownIcon, CornerRightUpIcon, CornerUpLeftIcon, CornerUpRightIcon, CpuIcon, CreditCardIcon, CropIcon, CrosshairIcon, DatabaseIcon, DeleteIcon, DiscIcon, DivideCircleIcon, DivideSquareIcon, DivideIcon, DollarSignIcon, DownloadCloudIcon, DownloadIcon, DribbbleIcon, DropletIcon, Edit2Icon, Edit3Icon, EditIcon, ExternalLinkIcon, EyeOffIcon, EyeIcon, FacebookIcon, FastForwardIcon, FeatherIcon, FigmaIcon, FileMinusIcon, FilePlusIcon, FileTextIcon, FileIcon, FilmIcon, FilterIcon, FlagIcon, FolderMinusIcon, FolderPlusIcon, FolderIcon, FramerIcon, FrownIcon, GiftIcon, GitBranchIcon, GitCommitIcon, GitMergeIcon, GitPullRequestIcon, GithubIcon, GitlabIcon, GlobeIcon, GridIcon, HardDriveIcon, HashIcon, HeadphonesIcon, HeartIcon, HelpCircleIcon, HexagonIcon, HomeIcon, ImageIcon, InboxIcon, InfoIcon, InstagramIcon, ItalicIcon, KeyIcon, LayersIcon, LayoutIcon, LifeBuoyIcon, Link2Icon, LinkIcon, LinkedinIcon, ListIcon, LoaderIcon, LockIcon, LogInIcon, LogOutIcon, MailIcon, MapPinIcon, MapIcon, Maximize2Icon, MaximizeIcon, MehIcon, MenuIcon, MessageCircleIcon, MessageSquareIcon, MicOffIcon, MicIcon, Minimize2Icon, MinimizeIcon, MinusCircleIcon, MinusSquareIcon, MinusIcon, MonitorIcon, MoonIcon, MoreHorizontalIcon, MoreVerticalIcon, MousePointerIcon, MoveIcon, MusicIcon, Navigation2Icon, NavigationIcon, OctagonIcon, PackageIcon, PaperclipIcon, PauseCircleIcon, PauseIcon, PenToolIcon, PercentIcon, PhoneCallIcon, PhoneForwardedIcon, PhoneIncomingIcon, PhoneMissedIcon, PhoneOffIcon, PhoneOutgoingIcon, PhoneIcon, PieChartIcon, PlayCircleIcon, PlayIcon, PlusCircleIcon, PlusSquareIcon, PlusIcon, PocketIcon, PowerIcon, PrinterIcon, RadioIcon, RefreshCcwIcon, RefreshCwIcon, RepeatIcon, RewindIcon, RotateCcwIcon, RotateCwIcon, RssIcon, SaveIcon, ScissorsIcon, SearchIcon, SendIcon, ServerIcon, SettingsIcon, Share2Icon, ShareIcon, ShieldOffIcon, ShieldIcon, ShoppingBagIcon, ShoppingCartIcon, ShuffleIcon, SidebarIcon, SkipBackIcon, SkipForwardIcon, SlackIcon, SlashIcon, SlidersIcon, SmartphoneIcon, SmileIcon, SpeakerIcon, SquareIcon, StarIcon, StopCircleIcon, SunIcon, SunriseIcon, SunsetIcon, TabletIcon, TagIcon, TargetIcon, TerminalIcon, ThermometerIcon, ThumbsDownIcon, ThumbsUpIcon, ToggleLeftIcon, ToggleRightIcon, ToolIcon, Trash2Icon, TrashIcon, TrelloIcon, TrendingDownIcon, TrendingUpIcon, TriangleIcon, TruckIcon, TvIcon, TwitchIcon, TwitterIcon, TypeIcon, UmbrellaIcon, UnderlineIcon, UnlockIcon, UploadCloudIcon, UploadIcon, UserCheckIcon, UserMinusIcon, UserPlusIcon, UserXIcon, UserIcon, UsersIcon, VideoOffIcon, VideoIcon, VoicemailIcon, Volume1Icon, Volume2Icon, VolumeXIcon, VolumeIcon, WatchIcon, WifiOffIcon, WifiIcon, WindIcon, XCircleIcon, XOctagonIcon, XSquareIcon, XIcon, YoutubeIcon, ZapOffIcon, ZapIcon, ZoomInIcon, ZoomOutIcon } from "@zhuowenli/vue-feather-icons";

import Layout from "../../layouts/main.vue";
import PageHeader from "@/components/page-header";
import appConfig from "../../../app.config";

export default {
    page: {
        title: "Feather",
        meta: [{ name: "description", content: appConfig.description }],
    },
    data() {
        return {
            title: "Feather",
            items: [
                {
                    text: "Icons",
                    href: "/",
                },
                {
                    text: "Feather",
                    active: true,
                },
            ],
        };
    },
    components: {
        Layout,
        PageHeader,
        ActivityIcon,
        AirplayIcon,
        AlertCircleIcon,
        AlertOctagonIcon,
        AlertTriangleIcon,
        AlignCenterIcon,
        AlignJustifyIcon,
        AlignLeftIcon,
        AlignRightIcon,
        AnchorIcon,
        ApertureIcon,
        ArchiveIcon,
        ArrowDownCircleIcon,
        ArrowDownLeftIcon,
        ArrowDownRightIcon,
        ArrowDownIcon,
        ArrowLeftCircleIcon,
        ArrowLeftIcon,
        ArrowRightCircleIcon,
        ArrowRightIcon,
        ArrowUpCircleIcon,
        ArrowUpLeftIcon,
        ArrowUpRightIcon,
        ArrowUpIcon,
        AtSignIcon,
        AwardIcon,
        BarChart2Icon,
        BarChartIcon,
        BatteryChargingIcon,
        BatteryIcon,
        BellOffIcon,
        BellIcon,
        BluetoothIcon,
        BoldIcon,
        BookOpenIcon,
        BookIcon,
        BookmarkIcon,
        BoxIcon,
        BriefcaseIcon,
        CalendarIcon,
        CameraOffIcon,
        CameraIcon,
        CastIcon,
        CheckCircleIcon,
        CheckSquareIcon,
        CheckIcon,
        ChevronDownIcon,
        ChevronLeftIcon,
        ChevronRightIcon,
        ChevronUpIcon,
        ChevronsDownIcon,
        ChevronsLeftIcon,
        ChevronsRightIcon,
        ChevronsUpIcon,
        ChromeIcon,
        CircleIcon,
        ClipboardIcon,
        ClockIcon,
        CloudDrizzleIcon,
        CloudLightningIcon,
        CloudOffIcon,
        CloudRainIcon,
        CloudSnowIcon,
        CloudIcon,
        CodeIcon,
        CodepenIcon,
        CodesandboxIcon,
        CoffeeIcon,
        ColumnsIcon,
        CommandIcon,
        CompassIcon,
        CopyIcon,
        CornerDownLeftIcon,
        CornerDownRightIcon,
        CornerLeftDownIcon,
        CornerLeftUpIcon,
        CornerRightDownIcon,
        CornerRightUpIcon,
        CornerUpLeftIcon,
        CornerUpRightIcon,
        CpuIcon,
        CreditCardIcon,
        CropIcon,
        CrosshairIcon,
        DatabaseIcon,
        DeleteIcon,
        DiscIcon,
        DivideCircleIcon,
        DivideSquareIcon,
        DivideIcon,
        DollarSignIcon,
        DownloadCloudIcon,
        DownloadIcon,
        DribbbleIcon,
        DropletIcon,
        Edit2Icon,
        Edit3Icon,
        EditIcon,
        ExternalLinkIcon,
        EyeOffIcon,
        EyeIcon,
        FacebookIcon,
        FastForwardIcon,
        FeatherIcon,
        FigmaIcon,
        FileMinusIcon,
        FilePlusIcon,
        FileTextIcon,
        FileIcon,
        FilmIcon,
        FilterIcon,
        FlagIcon,
        FolderMinusIcon,
        FolderPlusIcon,
        FolderIcon,
        FramerIcon,
        FrownIcon,
        GiftIcon,
        GitBranchIcon,
        GitCommitIcon,
        GitMergeIcon,
        GitPullRequestIcon,
        GithubIcon,
        GitlabIcon,
        GlobeIcon,
        GridIcon,
        HardDriveIcon,
        HashIcon,
        HeadphonesIcon,
        HeartIcon,
        HelpCircleIcon,
        HexagonIcon,
        HomeIcon,
        ImageIcon,
        InboxIcon,
        InfoIcon,
        InstagramIcon,
        ItalicIcon,
        KeyIcon,
        LayersIcon,
        LayoutIcon,
        LifeBuoyIcon,
        Link2Icon,
        LinkIcon,
        LinkedinIcon,
        ListIcon,
        LoaderIcon,
        LockIcon,
        LogInIcon,
        LogOutIcon,
        MailIcon,
        MapPinIcon,
        MapIcon,
        Maximize2Icon,
        MaximizeIcon,
        MehIcon,
        MenuIcon,
        MessageCircleIcon,
        MessageSquareIcon,
        MicOffIcon,
        MicIcon,
        Minimize2Icon,
        MinimizeIcon,
        MinusCircleIcon,
        MinusSquareIcon,
        MinusIcon,
        MonitorIcon,
        MoonIcon,
        MoreHorizontalIcon,
        MoreVerticalIcon,
        MousePointerIcon,
        MoveIcon,
        MusicIcon,
        Navigation2Icon,
        NavigationIcon,
        OctagonIcon,
        PackageIcon,
        PaperclipIcon,
        PauseCircleIcon,
        PauseIcon,
        PenToolIcon,
        PercentIcon,
        PhoneCallIcon,
        PhoneForwardedIcon,
        PhoneIncomingIcon,
        PhoneMissedIcon,
        PhoneOffIcon,
        PhoneOutgoingIcon,
        PhoneIcon,
        PieChartIcon,
        PlayCircleIcon,
        PlayIcon,
        PlusCircleIcon,
        PlusSquareIcon,
        PlusIcon,
        PocketIcon,
        PowerIcon,
        PrinterIcon,
        RadioIcon,
        RefreshCcwIcon,
        RefreshCwIcon,
        RepeatIcon,
        RewindIcon,
        RotateCcwIcon,
        RotateCwIcon,
        RssIcon,
        SaveIcon,
        ScissorsIcon,
        SearchIcon,
        SendIcon,
        ServerIcon,
        SettingsIcon,
        Share2Icon,
        ShareIcon,
        ShieldOffIcon,
        ShieldIcon,
        ShoppingBagIcon,
        ShoppingCartIcon,
        ShuffleIcon,
        SidebarIcon,
        SkipBackIcon,
        SkipForwardIcon,
        SlackIcon,
        SlashIcon,
        SlidersIcon,
        SmartphoneIcon,
        SmileIcon,
        SpeakerIcon,
        SquareIcon,
        StarIcon,
        StopCircleIcon,
        SunIcon,
        SunriseIcon,
        SunsetIcon,
        TabletIcon,
        TagIcon,
        TargetIcon,
        TerminalIcon,
        ThermometerIcon,
        ThumbsDownIcon,
        ThumbsUpIcon,
        ToggleLeftIcon,
        ToggleRightIcon,
        ToolIcon,
        Trash2Icon,
        TrashIcon,
        TrelloIcon,
        TrendingDownIcon,
        TrendingUpIcon,
        TriangleIcon,
        TruckIcon,
        TvIcon,
        TwitchIcon,
        TwitterIcon,
        TypeIcon,
        UmbrellaIcon,
        UnderlineIcon,
        UnlockIcon,
        UploadCloudIcon,
        UploadIcon,
        UserCheckIcon,
        UserMinusIcon,
        UserPlusIcon,
        UserXIcon,
        UserIcon,
        UsersIcon,
        VideoOffIcon,
        VideoIcon,
        VoicemailIcon,
        Volume1Icon,
        Volume2Icon,
        VolumeXIcon,
        VolumeIcon,
        WatchIcon,
        WifiOffIcon,
        WifiIcon,
        WindIcon,
        XCircleIcon,
        XOctagonIcon,
        XSquareIcon,
        XIcon,
        YoutubeIcon,
        ZapOffIcon,
        ZapIcon,
        ZoomInIcon,
        ZoomOutIcon
    },
};
</script>

<template>
    <Layout>
        <PageHeader :title="title" :items="items" />
        <b-row>
            <b-col cols="12">
                <b-card no-body>
                    <b-card-header>
                        <b-card-title>Examples</b-card-title>
                        <p class="text-muted mb-0">
                            Use
                            <code>&lt;i data-feather="**">&lt;/i></code> class.
                        </p>
                    </b-card-header>
                    <b-card-body class="pt-0">
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <ActivityIcon></ActivityIcon>activity
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon></AirplayIcon>airplay
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AlertCircleIcon></AlertCircleIcon>alert-circle
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AlertOctagonIcon></AlertOctagonIcon>AlertOctagonIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AlertTriangleIcon></AlertTriangleIcon>AlertTriangleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AlignCenterIcon></AlignCenterIcon>AlignCenterIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AlignJustifyIcon></AlignJustifyIcon>AlignJustifyIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AlignLeftIcon></AlignLeftIcon>AlignLeftIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AlignRightIcon></AlignRightIcon>AlignRightIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AnchorIcon></AnchorIcon>AnchorIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ApertureIcon></ApertureIcon>ApertureIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArchiveIcon></ArchiveIcon>ArchiveIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArrowDownCircleIcon></ArrowDownCircleIcon>ArrowDownCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArrowDownLeftIcon></ArrowDownLeftIcon>ArrowDownLeftIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArrowDownRightIcon></ArrowDownRightIcon>ArrowDownRightIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArrowDownIcon></ArrowDownIcon>ArrowDownIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArrowLeftCircleIcon></ArrowLeftCircleIcon>ArrowLeftCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArrowLeftIcon></ArrowLeftIcon>ArrowLeftIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArrowRightCircleIcon></ArrowRightCircleIcon>ArrowRightCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArrowRightIcon></ArrowRightIcon>ArrowRightIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArrowUpCircleIcon></ArrowUpCircleIcon>ArrowUpCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArrowUpLeftIcon></ArrowUpLeftIcon>ArrowUpLeftIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArrowUpRightIcon></ArrowUpRightIcon>ArrowUpRightIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArrowUpIcon></ArrowUpIcon>ArrowUpIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AtSignIcon></AtSignIcon>AtSignIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AwardIcon></AwardIcon>AwardIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <BarChart2Icon></BarChart2Icon>BarChart2Icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <BarChartIcon></BarChartIcon>BarChartIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <BatteryChargingIcon></BatteryChargingIcon>BatteryChargingIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <BatteryIcon></BatteryIcon>BatteryIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <BellOffIcon></BellOffIcon>BellOffIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <BellIcon></BellIcon>BellIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <BluetoothIcon></BluetoothIcon>BluetoothIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <BoldIcon></BoldIcon>BoldIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <BookOpenIcon></BookOpenIcon>BookOpenIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <BookIcon></BookIcon>BookIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <BookmarkIcon></BookmarkIcon>BookmarkIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <BoxIcon></BoxIcon>BoxIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <BriefcaseIcon></BriefcaseIcon>BriefcaseIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CalendarIcon></CalendarIcon>CalendarIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CameraOffIcon></CameraOffIcon>CameraOffIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CameraIcon></CameraIcon>CameraIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CastIcon></CastIcon>CastIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CheckCircleIcon></CheckCircleIcon>CheckCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CheckSquareIcon></CheckSquareIcon>CheckSquareIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CheckIcon></CheckIcon>CheckIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ChevronDownIcon></ChevronDownIcon>ChevronDownIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ChevronLeftIcon></ChevronLeftIcon>ChevronLeftIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ChevronRightIcon></ChevronRightIcon>ChevronRightIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ChevronUpIcon></ChevronUpIcon>ChevronUpIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ChevronsDownIcon></ChevronsDownIcon>ChevronsDownIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ChevronsLeftIcon></ChevronsLeftIcon>ChevronsLeftIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ChevronsRightIcon></ChevronsRightIcon>ChevronsRightIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ChevronsUpIcon></ChevronsUpIcon>ChevronsUpIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ChromeIcon></ChromeIcon>ChromeIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CircleIcon></CircleIcon>CircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ClipboardIcon></ClipboardIcon>ClipboardIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ClockIcon></ClockIcon>ClockIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CloudDrizzleIcon></CloudDrizzleIcon>CloudDrizzleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CloudLightningIcon></CloudLightningIcon>CloudLightningIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CloudOffIcon></CloudOffIcon>CloudOffIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CloudRainIcon></CloudRainIcon>CloudRainIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CloudSnowIcon></CloudSnowIcon>CloudSnowIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CloudIcon></CloudIcon>CloudIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CodeIcon></CodeIcon>CodeIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CodepenIcon></CodepenIcon>CodepenIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CodesandboxIcon></CodesandboxIcon>CodesandboxIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CoffeeIcon></CoffeeIcon>CoffeeIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ColumnsIcon></ColumnsIcon>ColumnsIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CommandIcon></CommandIcon>CommandIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CompassIcon></CompassIcon>CompassIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CopyIcon></CopyIcon>CopyIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CornerDownLeftIcon></CornerDownLeftIcon>CornerDownLeftIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CornerDownRightIcon></CornerDownRightIcon>CornerDownRightIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CornerLeftDownIcon></CornerLeftDownIcon>CornerLeftDownIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CornerLeftUpIcon></CornerLeftUpIcon>CornerLeftUpIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CornerRightDownIcon></CornerRightDownIcon>CornerRightDownIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CornerRightUpIcon></CornerRightUpIcon>CornerRightUpIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CornerUpLeftIcon></CornerUpLeftIcon>CornerUpLeftIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CornerUpRightIcon></CornerUpRightIcon>CornerUpRightIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CpuIcon></CpuIcon>CpuIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CreditCardIcon></CreditCardIcon>CreditCardIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CropIcon></CropIcon>CropIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <CrosshairIcon></CrosshairIcon>CrosshairIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <DatabaseIcon></DatabaseIcon>DatabaseIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <DeleteIcon></DeleteIcon>DeleteIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <DiscIcon></DiscIcon>DiscIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <DivideCircleIcon></DivideCircleIcon>DivideCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <DivideSquareIcon></DivideSquareIcon>DivideSquareIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <DivideIcon></DivideIcon>DivideIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <DollarSignIcon></DollarSignIcon>DollarSignIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <DownloadCloudIcon></DownloadCloudIcon>DownloadCloudIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <DownloadIcon></DownloadIcon>DownloadIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <DribbbleIcon></DribbbleIcon>DribbbleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <DropletIcon></DropletIcon>DropletIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <Edit2Icon></Edit2Icon>Edit2Icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <Edit3Icon></Edit3Icon>Edit3Icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <EditIcon></EditIcon>EditIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ExternalLinkIcon></ExternalLinkIcon>ExternalLinkIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <EyeOffIcon></EyeOffIcon>EyeOffIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <EyeIcon></EyeIcon>EyeIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FacebookIcon></FacebookIcon>FacebookIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FastForwardIcon></FastForwardIcon>FastForwardIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FeatherIcon></FeatherIcon>FeatherIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FigmaIcon></FigmaIcon>FigmaIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FileMinusIcon></FileMinusIcon>FileMinusIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FilePlusIcon></FilePlusIcon>FilePlusIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FileTextIcon></FileTextIcon>FileTextIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FileIcon></FileIcon>FileIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FilmIcon></FilmIcon>FilmIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FilterIcon></FilterIcon>FilterIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FlagIcon></FlagIcon>FlagIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FolderMinusIcon></FolderMinusIcon>FolderMinusIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FolderPlusIcon></FolderPlusIcon>FolderPlusIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FolderIcon></FolderIcon>FolderIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FramerIcon></FramerIcon>FramerIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <FrownIcon></FrownIcon>FrownIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <GiftIcon></GiftIcon>GiftIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <GitBranchIcon></GitBranchIcon>GitBranchIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <GitCommitIcon></GitCommitIcon>GitCommitIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <GitMergeIcon></GitMergeIcon>GitMergeIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <GitPullRequestIcon></GitPullRequestIcon>GitPullRequestIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <GithubIcon></GithubIcon>GithubIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <GitlabIcon></GitlabIcon>GitlabIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <GlobeIcon></GlobeIcon>GlobeIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <GridIcon></GridIcon>GridIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <HardDriveIcon></HardDriveIcon>HardDriveIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <HashIcon></HashIcon>HashIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <HeadphonesIcon></HeadphonesIcon>HeadphonesIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <HeartIcon></HeartIcon>HeartIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <HelpCircleIcon></HelpCircleIcon>HelpCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <HexagonIcon></HexagonIcon>HexagonIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <HomeIcon></HomeIcon>HomeIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ImageIcon></ImageIcon>ImageIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <InboxIcon></InboxIcon>InboxIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <InfoIcon></InfoIcon>InfoIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <InstagramIcon></InstagramIcon>InstagramIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ItalicIcon></ItalicIcon>ItalicIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <KeyIcon></KeyIcon>KeyIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <LayersIcon></LayersIcon>LayersIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <LayoutIcon></LayoutIcon>LayoutIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <LifeBuoyIcon></LifeBuoyIcon>LifeBuoyIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <Link2Icon></Link2Icon>Link2Icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <LinkIcon></LinkIcon>LinkIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <LinkedinIcon></LinkedinIcon>LinkedinIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ListIcon></ListIcon>ListIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <LoaderIcon></LoaderIcon>LoaderIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <LockIcon></LockIcon>LockIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <LogInIcon></LogInIcon>LogInIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <LogOutIcon></LogOutIcon>LogOutIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MailIcon></MailIcon>MailIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MapPinIcon></MapPinIcon>MapPinIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MapIcon></MapIcon>MapIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <Maximize2Icon></Maximize2Icon>Maximize2Icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MaximizeIcon></MaximizeIcon>MaximizeIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MehIcon></MehIcon>MehIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MenuIcon></MenuIcon>MenuIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MessageCircleIcon></MessageCircleIcon>MessageCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MessageSquareIcon></MessageSquareIcon>MessageSquareIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MicOffIcon></MicOffIcon>MicOffIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MicIcon></MicIcon>MicIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <Minimize2Icon></Minimize2Icon>Minimize2Icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MinimizeIcon></MinimizeIcon>MinimizeIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MinusCircleIcon></MinusCircleIcon>MinusCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MinusSquareIcon></MinusSquareIcon>MinusSquareIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MinusIcon></MinusIcon>MinusIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MonitorIcon></MonitorIcon>MonitorIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MoonIcon></MoonIcon>MoonIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MoreHorizontalIcon></MoreHorizontalIcon>MoreHorizontalIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MoreVerticalIcon></MoreVerticalIcon>MoreVerticalIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MousePointerIcon></MousePointerIcon>MousePointerIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MoveIcon></MoveIcon>MoveIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <MusicIcon></MusicIcon>MusicIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <Navigation2Icon></Navigation2Icon>Navigation2Icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <NavigationIcon></NavigationIcon>NavigationIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <OctagonIcon></OctagonIcon>OctagonIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PackageIcon></PackageIcon>PackageIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PaperclipIcon></PaperclipIcon>PaperclipIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PauseCircleIcon></PauseCircleIcon>PauseCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PauseIcon></PauseIcon>PauseIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PenToolIcon></PenToolIcon>PenToolIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PercentIcon></PercentIcon>PercentIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PhoneCallIcon></PhoneCallIcon>PhoneCallIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PhoneForwardedIcon></PhoneForwardedIcon>PhoneForwardedIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PhoneIncomingIcon></PhoneIncomingIcon>PhoneIncomingIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PhoneMissedIcon></PhoneMissedIcon>PhoneMissedIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PhoneOffIcon></PhoneOffIcon>PhoneOffIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PhoneOutgoingIcon></PhoneOutgoingIcon>PhoneOutgoingIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PhoneIcon></PhoneIcon>PhoneIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PieChartIcon></PieChartIcon>PieChartIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PlayCircleIcon></PlayCircleIcon>PlayCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PlayIcon></PlayIcon>PlayIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PlusCircleIcon></PlusCircleIcon>PlusCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PlusSquareIcon></PlusSquareIcon>PlusSquareIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PlusIcon></PlusIcon>PlusIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PocketIcon></PocketIcon>PocketIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PowerIcon></PowerIcon>PowerIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <PrinterIcon></PrinterIcon>PrinterIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <RadioIcon></RadioIcon>RadioIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <RefreshCcwIcon></RefreshCcwIcon>RefreshCcwIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <RefreshCwIcon></RefreshCwIcon>RefreshCwIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <RepeatIcon></RepeatIcon>RepeatIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <RewindIcon></RewindIcon>RewindIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <RotateCcwIcon></RotateCcwIcon>RotateCcwIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <RotateCwIcon></RotateCwIcon>RotateCwIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <RssIcon></RssIcon>RssIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SaveIcon></SaveIcon>SaveIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ScissorsIcon></ScissorsIcon>ScissorsIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SearchIcon></SearchIcon>SearchIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SendIcon></SendIcon>SendIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ServerIcon></ServerIcon>ServerIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SettingsIcon></SettingsIcon>SettingsIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <Share2Icon></Share2Icon>Share2Icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ShareIcon></ShareIcon>ShareIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ShieldOffIcon></ShieldOffIcon>ShieldOffIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ShieldIcon></ShieldIcon>ShieldIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ShoppingBagIcon></ShoppingBagIcon>ShoppingBagIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ShoppingCartIcon></ShoppingCartIcon>ShoppingCartIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ShuffleIcon></ShuffleIcon>ShuffleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SidebarIcon></SidebarIcon>SidebarIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SkipBackIcon></SkipBackIcon>SkipBackIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SkipForwardIcon></SkipForwardIcon>SkipForwardIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SlackIcon></SlackIcon>SlackIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SlashIcon></SlashIcon>SlashIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SlidersIcon></SlidersIcon>SlidersIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SmartphoneIcon></SmartphoneIcon>SmartphoneIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SmileIcon></SmileIcon>SmileIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SpeakerIcon></SpeakerIcon>SpeakerIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SquareIcon></SquareIcon>SquareIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <StarIcon></StarIcon>StarIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <StopCircleIcon></StopCircleIcon>StopCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SunIcon></SunIcon>SunIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SunriseIcon></SunriseIcon>SunriseIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <SunsetIcon></SunsetIcon>SunsetIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TabletIcon></TabletIcon>TabletIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TagIcon></TagIcon>TagIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TargetIcon></TargetIcon>TargetIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TerminalIcon></TerminalIcon>TerminalIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ThermometerIcon></ThermometerIcon>ThermometerIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ThumbsDownIcon></ThumbsDownIcon>ThumbsDownIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ThumbsUpIcon></ThumbsUpIcon>ThumbsUpIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ToggleLeftIcon></ToggleLeftIcon>ToggleLeftIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ToggleRightIcon></ToggleRightIcon>ToggleRightIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ToolIcon></ToolIcon>ToolIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <Trash2Icon></Trash2Icon>Trash2Icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TrashIcon></TrashIcon>TrashIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TrelloIcon></TrelloIcon>TrelloIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TrendingDownIcon></TrendingDownIcon>TrendingDownIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TrendingUpIcon></TrendingUpIcon>TrendingUpIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TriangleIcon></TriangleIcon>TriangleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TruckIcon></TruckIcon>TruckIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TvIcon></TvIcon>TvIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TwitchIcon></TwitchIcon>TwitchIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TwitterIcon></TwitterIcon>TwitterIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <TypeIcon></TypeIcon>TypeIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <UmbrellaIcon></UmbrellaIcon>UmbrellaIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <UnderlineIcon></UnderlineIcon>UnderlineIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <UnlockIcon></UnlockIcon>UnlockIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <UploadCloudIcon></UploadCloudIcon>UploadCloudIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <UploadIcon></UploadIcon>UploadIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <UserCheckIcon></UserCheckIcon>UserCheckIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <UserMinusIcon></UserMinusIcon>UserMinusIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <UserPlusIcon></UserPlusIcon>UserPlusIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <UserXIcon></UserXIcon>UserXIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <UserIcon></UserIcon>UserIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <UsersIcon></UsersIcon>UsersIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <VideoOffIcon></VideoOffIcon>VideoOffIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <VideoIcon></VideoIcon>VideoIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <VoicemailIcon></VoicemailIcon>VoicemailIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <Volume1Icon></Volume1Icon>Volume1Icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <Volume2Icon></Volume2Icon>Volume2Icon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <VolumeXIcon></VolumeXIcon>VolumeXIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <VolumeIcon></VolumeIcon>VolumeIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <WatchIcon></WatchIcon>WatchIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <WifiOffIcon></WifiOffIcon>WifiOffIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <WifiIcon></WifiIcon>WifiIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <WindIcon></WindIcon>WindIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <XCircleIcon></XCircleIcon>XCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <XOctagonIcon></XOctagonIcon>XOctagonIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <XSquareIcon></XSquareIcon>XSquareIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <XIcon></XIcon>XIcon,
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <YoutubeIcon></YoutubeIcon>YoutubeIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ZapOffIcon></ZapOffIcon>ZapOffIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ZapIcon></ZapIcon>ZapIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ZoomInIcon></ZoomInIcon>ZoomInIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ZoomOutIcon></ZoomOutIcon>ZoomOutIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon></AirplayIcon>AirplayIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon></AirplayIcon>AirplayIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon></AirplayIcon>AirplayIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon></AirplayIcon>AirplayIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon></AirplayIcon>AirplayIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon></AirplayIcon>AirplayIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon></AirplayIcon>AirplayIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AlertCircleIcon></AlertCircleIcon>AlertCircleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AlertOctagonIcon></AlertOctagonIcon>AlertOctagonIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AlertTriangleIcon></AlertTriangleIcon>AlertTriangleIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <AnchorIcon></AnchorIcon>AnchorIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ApertureIcon></ApertureIcon>ApertureIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ArchiveIcon></ArchiveIcon>ArchiveIcon
                            </b-col>
                            <b-col xl="3" lg="4" sm="6">
                                <ClockIcon></ClockIcon>ClockIcon
                            </b-col>
                        </b-row>
                        
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col cols="12">
                <b-card no-body>
                    <b-card-header>
                        <b-card-title>Sizes</b-card-title>
                        <p class="text-muted mb-0">
                            Use
                            <code>&lt;i data-feather="activity" class="icon-**"&gt;&lt;/i&gt;</code>. Available sizes
                            <code>xs, sm,md,lg,xl,xxl</code>
                        </p>
                    </b-card-header>
                    <b-card-body class="pt-0">
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon class="icon-xs"></AirplayIcon>airplay
                            </b-col>

                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon class="icon-sm"></AirplayIcon>airplay
                            </b-col>

                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon class="icon-md"></AirplayIcon>airplay
                            </b-col>

                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon class="icon-lg"></AirplayIcon>airplay
                            </b-col>

                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon class="icon-xl"></AirplayIcon>airplay
                            </b-col>

                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon class="icon-xxl"></AirplayIcon>airplay
                            </b-col>
                        </b-row>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>

        <b-row>
            <b-col cols="12">
                <b-card no-body>
                    <b-card-header>
                        <b-card-title>Two Tones Color Icons</b-card-title>
                        <p class="text-muted mb-0">
                            Use
                            <code>&lt;i data-feather="activity" class="icon-dual-**"&gt;&lt;/i&gt;</code>.
                        </p>
                    </b-card-header>
                    <b-card-body class="pt-0">
                        <b-row class="icon-demo-content">
                            <b-col xl="3" lg="4" sm="6">
                                <AirplayIcon class="icon-dual"></AirplayIcon>airplay
                            </b-col>

                            <b-col xl="3" lg="4" sm="6">
                                <AlertCircleIcon class="icon-dual-primary"></AlertCircleIcon>alert-circle
                            </b-col>

                            <b-col xl="3" lg="4" sm="6">
                                <AlertOctagonIcon class="icon-dual-success"></AlertOctagonIcon>alert-octagon
                            </b-col>

                            <b-col xl="3" lg="4" sm="6">
                                <AlertTriangleIcon class="icon-dual-info"></AlertTriangleIcon>alert-triangle
                            </b-col>

                            <b-col xl="3" lg="4" sm="6">
                                <AnchorIcon class="icon-dual-warning"></AnchorIcon>anchor
                            </b-col>

                            <b-col xl="3" lg="4" sm="6">
                                <ApertureIcon class="icon-dual-danger"></ApertureIcon>aperture
                            </b-col>

                            <b-col xl="3" lg="4" sm="6">
                                <ArchiveIcon class="icon-dual-dark"></ArchiveIcon>archive
                            </b-col>

                            <b-col xl="3" lg="4" sm="6">
                                <ClockIcon class="icon-dual-secondary"></ClockIcon>clock
                            </b-col>
                        </b-row>
                    </b-card-body>
                </b-card>
            </b-col>
        </b-row>
    </Layout>
</template>
