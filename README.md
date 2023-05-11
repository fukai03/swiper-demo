## 轮播图组件示例demo
> 后续可继续进行功能完善，如：自定义动画、自定义分页器、自定义导航按钮等
* 基于[swiper](https://github.com/nolimits4web/swiper)进行组件封装
* 组件文件夹：src/components/swiper、
  


demo启动方式：
```bash
npm install
npm run dev
```

接口
```ts
interface IAutoPlayProps {
    isAutoplay: boolean;
    delay: number;
    disableOnInteraction: boolean;
    pauseOnMouseEnter: boolean;
}
interface INavigationProps {
    isNavigation: boolean;
    leftIcon: string;
    rightIcon: string;
    left: CSSProperties['left'];
    right: CSSProperties['right'];
    iconWidth?: CSSProperties['width'];
    iconHeight?: CSSProperties['height'];
}
interface IPaginationProps {
    isPagination: boolean;
    clickable: boolean;
}

interface ISwiperProps {
    children: React.ReactElement[];
    autoplay?: Partial<IAutoPlayProps>;
    className?: string;
    navigation?: Partial<INavigationProps>;
    pagination?: Partial<IPaginationProps>;
    slidesPerView?: number;
    spaceBetween?: number;
    onSwiper?: (swiper: any) => void;
    onSlideChange?: (swiper: any) => void;
}
```
