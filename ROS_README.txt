# run stereo usb_cam
roslaunch usb_cam stereo_usb_cam_stream_publisher.launch
#run stereo_image_proc 
roslaunch stereo_image_proc stereo_image_proc_stream_publisher.launch

rosrun image_view stereo_view stereo:=/stereo_camera image:=image_rect _approximate_sync:=True _queue_size:=10


rosrun rqt_graph rqt_graph

rosrun rqt_reconfigure rqt_reconfigure